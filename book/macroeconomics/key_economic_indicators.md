## Key Economic Indicators
Just as how doctors require tools like thermometers to give a quantitative measure of the health of an individual, economic indicators are required to describe and assess the macroeconomy. These economic indicators are used to measure _relative_ economic performance between countries(__international comparison__), or comparing the economic performance of a single country as time progresses (__intertemporal comparison__).

### Size of the Economy

Economists use the concept of __national income__ to measure the size of the economy. National income is proportional to the amount of economy activity within the country, and therefore ceteris paribus, the greater the national income, the greater the level of economic activity. 

#### Gross Domestic Product (GDP)
> Nominal GDP is the sum of the market value of all _final_ goods and services produced _within a country_ over a given period of time (usually a year)
> $$GDP = \sum{P_x\times Q_x}$$

The goods and services here are final goods and services, because the inclusion of semi-finished goods would result in a miscalculation, specifically __double counting__, where the market value of semi-finished goods are included along with the market value of the its final form.

As the term "domestic" implies, this number will only include economic activity (production) within the country. Whether the goods produced within the country are consumed by local or foreign households however does not matter.

#### Real GDP
However, a nominal GDP increase does not necessarily indicate a healthy economy. Notice there are two terms in the formulation of GDP, $P_x$ and $Q_x$. This would mean that a GDP increase could be solely due to an increase in general price levels, and not output levels. 

To better determine if economic growth was a result of increase in output levels, economists use the concept of __real GDP__. This is achieved by multiplying the value of output each year with the prices of those goods _in some predetermined year_. This year is known as the __base year__, and the price prevailing at that period of time is the __base year price__ of the good.

$$\text{Real GDP} = \sum{P_{byp}\times Q_x}$$

#### Gross National Product (GNP)
While GDP measure the market value of final goods and services _produced within the country_, the GNP measures the market value of final goods and services _produced by citizens of the country_, __regardless of where they reside__.

$$\text{GNP} = \text{GDP} - \text{net factor (property) income from abroad}$$

The concept of GNP is important when many of the citizens of a country reside overseas, of which the income they generate overseas are repatriated to back to their home country. The value of the GDP will then be vastly different from that of the value of the GNP.

#### Net National Product (NNP)
The NNP is used by economists to recognise that some of the capital stock used suffer from wear and tear and require replacement. Capital stocks include items such as machinery and equipment. This would mean that the NNP would provide a better indication of the increase in productive capacity.

$$\text{NNP} = \text{GNP} - \text{Depreciation}$$

Depreciation is also sometimes termed as __capital consumption__ and __replacement investment__.

#### Making Comparisons
##### Intertemporal Comparisons
###### Measuring Economic Growth
To measure economic growth (this phrase is already a first derivative;"change in economic activity over time"), economists calculate the _percentage change_ of GDP:

$$\% \Delta \text{GDP}_x = \left(\frac{\text{GDP}_x-\text{GDP}_{x-1}}{\text{GDP}_{x-1}}\right)\times 100\%$$

###### Accounting for Population Changes
While GDP is an indication of the total economic activity of the country, it is not indicative of the amount of income received per person in the population on average. This information is important as it gives economists an idea of how much "richer" each individual on average is. To account for the population changes, economists use the concept of __GDP per capita__.

Mathematically we write:

$$\text{GDP per capita} = \frac{\text{GDP}}{\text{population}}$$

We can approximate changes in per capita GDP by differentiating both sides by time.

$$\frac{d\text{GDP per capita}}{dt} \approx \frac{\frac{d\text{GDP}}{dt}\times\text{population} - \text{GDP}\times\frac{d\text{population}}{dt}}{\text{population}^2}$$

$$\frac{\frac{d\text{GDP per capita}}{dt}}{\text{GDP per capita}}\times 100\%\approx \frac{\frac{d\text{GDP}}{dt}\times\text{population} - \text{GDP}\times\frac{d\text{population}}{dt}}{\text{population}^2\times \frac{\text{GDP}}{\text{population}}}\times 100\%$$

Rearranging the terms, we get:

$$\% \Delta \text{GDP per capita} \approx \% \Delta\text{GDP} -\% \Delta\text{population}$$

The higher the GDP per capita, the greater the income earned on average per person. This means that the purchasing power of the people in the country have risen, ceteris paribus. This does not hold if the inflation rate is greater than the rate of increase in real GDP per capita.

##### International Comparison

###### Comparing Economic Size Across Countries
One issue economists face when compaing economic size across countries is that GDP is often measured based on local currency. To overcome this problem economists convert each country's GDP to be expressed in a common currency, often the USD.

###### Comparing Purchasing Power Across Countries
The problem with the traditional approach of converting to the common currency for comparing purchasing power across countries using market exchange rate is that _prices of goods are different in different countries_. A packet of oreos may cost 1 dollar in Singapore, but 10 dollars in the US, and the exchange rate is not 1:10. More appropriately, the prices of goods and services in different countries are not sufficiently similar to make such a fleeting comparison.

To resolve this issue, economists construct an artificial "exchange rate" that is based on the average prices of common goods and services across countries, termed as the "__purchasing power parity (PPP) exchange rate__".

The construction of the PPP exchange rate for all countries can be problematic. 

__FILL THIS UP__

To make an accurate comparison of purchasing power across countries, economists then use the PPP GDP per capita.

### Inflation
In addition to the size of the economy, economists also concern themselves with other health indicators of the economy, among which include inflation.

Inflation is defined as the following:

> Inflation is a __sustained and inordinate__ increase in the general price level.

Inflation rate is the percentage increase in the general price level.

To measure inflation, economists use 2 indicators, the GDP deflator and the consumer price index (CPI).

#### GDP Deflator
$$\text{GDP Deflator}=\frac{\text{nominal GDP}}{\text{real GDP}} \times 100$$

The GDP deflator is an index, and thus is dimensionless. Notice that by definition, the nominal and real GDP are equal in the base year. It then follows that the _GDP deflator has a value of 100 at the base year_.

To find the inflation rate (in the case of the GDP deflator, the percentage increase in the _weighted_ average price of goods and services), we perform a familiar calculation:

$$\left(\frac{d_x-d_{x-1}}{d_{x-1}}\right)\times 100\%$$

where $d_x$ is the GDP deflator index value at year $x$.

#### Consumer Price Index (CPI)
The CPI is constructed using a common basket of goods and services that describes the general consumption pattern of the society. The consumption pattern and basket of goods and services are determined often through mass compulsory surveys and phone interviews. The prices of these goods and services are then recorded and assigned to be the base year. Some goods are purchased more than others, and thus take more weightage in the calculation of the CPI. The CPI is an _expenditure-weighted average_ of the prices of the goods and services selected.

High inflation is undesirable for a country.

__TBC__
