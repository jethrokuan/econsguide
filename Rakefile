require 'rake'

desc "Build all output targets, commit, and push a new release"
task :release => "build:all" do
  Releaser.new.release
end

desc "Prepare output directory"
task :prepare do
  Builder.new.prepare_output_directory
end

namespace :push do
  task :website do
    Builder.new.push_website
  end
end

namespace :build do
  task :markdown => :prepare do
    Builder.new.generate_markdown
  end

  task :html => [:prepare, :markdown] do
    Builder.new.generate_html
  end

  task :pdf => [:prepare, :markdown] do
    Builder.new.generate_pdf
  end

  task :latex => [:prepare, :markdown] do
    Builder.new.generate_latex
  end

  task :epub => [:prepare, :markdown] do
    Builder.new.generate_epub
  end

  task :sample => [:prepare] do
    Builder.new.generate_sample
  end

  desc "Build all output targets"
  task :all => [:html, :pdf, :epub] do
  end
end

module Runner
  private

  def run(command)
    puts "  + #{command}" if ENV['verbose']
    if ENV['verbose']
      puts "  - #{system command}"
    else
      system command
    end
  end
end

class Builder
  OUTPUT_DIR = "output"
  WEBSITE_DIR = "output/html"

  include Runner

  attr_accessor :output

  def parse_file(output, filename)
    file = File.open(filename)
    file.each do |line| 
      if line =~ /\<\<\((.+)\)/
        output.puts "````"
        parse_file(output, "#{File.dirname(filename)}/#{$1}")
        output.puts "````"
      elsif line =~ /\<\<\[(.+)\]/
        parse_file(output, "#{File.dirname(filename)}/#{$1}")
      else
        output.puts line
      end
    end
  end

  def prepare_output_directory
    puts "## Prepping output dir..."
    run "mkdir output" if !File.exists? "output"
    run "rm -rf output/*"
    run "mkdir output/html/"
    run "cp -r book/images output"
    run "cp -r book/images output/html"
  end

  def push_website
    Dir.chdir WEBSITE_DIR do
      run "git init ."
      run "git add -A"
      run "git commit -m 'New Push'"
      run "heroku git:remote -a econsguide"
      run "git push -f heroku master"
    end
  end

  def generate_markdown
    puts "## Building master Markdown book..."
    markdown = File.new("output/book.md", "w+")
    parse_file(markdown, "book/book.md")
    markdown.close
  end

  def generate_html
    Dir.chdir OUTPUT_DIR do
      puts "## Generating HTML version..."
      working = File.expand_path File.dirname(__FILE__)
      work = working.inspect
      run "cp -r ../html_base/. html"
      run "pandoc book.md --data-dir=#{work} --toc-depth=2 --template=template -c css/layout.css --mathjax --section-divs --toc --standalone -t html5 -o html/index.html"
    end
  end

  def generate_pdf
    Dir.chdir OUTPUT_DIR do
      working = File.expand_path File.dirname(__FILE__)
      work = working.inspect
      puts "## Generating PDF version"
      run "pandoc book.md --data-dir=#{work} --template=template --chapters --toc -o book.pdf"
    end
  end

  def generate_latex
    Dir.chdir OUTPUT_DIR do
      puts "## Generating LaTeX version..."
      working = File.expand_path File.dirname(__FILE__)
      work = working.inspect
      run "pandoc book.md --data-dir=#{work} --template=template --chapters --toc -o book.latex"
    end
  end

  def generate_epub
    Dir.chdir OUTPUT_DIR do
      puts "## Generating EPUB version..."
      # run "convert -density 400 -resize 1000x1000 images/cover.pdf images/cover.png"
      # run "pandoc book.md --toc --epub-cover-image=images/cover.png -o book.epub"
      run "pandoc book.md --toc -o book.epub"
    end
  end
end
