ECONOMICS: A COMPREHENSIVE GUIDE
================================

# Setup
1. Install [pandoc](https://code.google.com/p/pandoc/downloads/list).
2. Install LaTeX. For Mac Users install [BasicTex](http://mirror.ctan.org/systems/mac/mactex/mactex-basic.pkg), and for Windows Users install [MikTex](http://miktex.org/). Install missing packages using the `tlmgr` command line tool for Mac Users.

# Generating Files
The files are compiled from the markdown format using pandoc. A rake task has been created for the creation of the `pdf`, `html` and `epub` filetypes.

Their respective rake tasks are:
1. `rake build:pdf`
2. `rake build:epub`
3. `rake build:html`

To build all three types, just run `rake build:all`

Support for mobi has been dropped who uses that anyway.

#Pushing up to Heroku
To push the website to Heroku run: `rake push:website`. You must have the permissions to push to the repository. It's based off the PHP/Apache stack to serve the static files with a smart PHP 1 line hack :D

#Disclaimer
The content provided here might not be a 100% accurate. We hope to receive pull requests/feedback on errors. Thanks in advance!
