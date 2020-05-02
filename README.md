# Analyzing-Profitability-on-Short-Term-Rentals-using-AirbnB-and-Zillow-Data

https://rpubs.com/shreyjparth/607800

### Problem Statement: 
To analyze the given data to identify the zipcodes in New York that are worth investing for most profit on short term rentals.


### Data Available:
For this purpose, publicly available data from Zillow and AirBnB were used.

* 1)**Cost data**: Zillow provides us an estimate of value for two-bedroom properties.

* 2)**Revenue data**: AirBnB is the medium through which the investor plans to lease out their investment property.


### Language and Tool Used:
The analysis has been purely done on R and a notebook has been created using R Markdown.


Packages Used:
* Naniar- handling missing values
* Tidyverse- Cleaning the data
* DataExplorer - Automated data exploration 
* Corrplot - Plotting correlation of variables
* Readr - Reading and loading data files
* Tidyr - Cleaning the data
* Ggplot2 - Creating plots and visualizations
* Plotly - Creating interactive plots and visualizations
* KableExtra - Creating/showing dataframe in tabular form


Assumptions:
* The investor will pay for the property in cash (i.e. no mortgage/interest rate will need to be accounted for).
* The time value of money discount rate is 0% (i.e. $1 today is worth the same 100 years from now).
* All properties and all square feet within each locale can be assumed to be homogeneous (i.e. a 1000 square foot   property     in a locale such as Bronx or Manhattan generates twice the revenue and costs twice as much as any other   500 square foot     property within that same locale.)
* The room types 'Entire house' and 'Private room' are considered the same. The price given for the stay at the    property     is considered the total price irrespective of the room type.
* Availability for next 365 days is a considered as the metric for occupancy. Lesser than availability , higher the             occupancy.
* Occupancy rate is calculated by subtracting the total available days by total number of days in year and         dividing     it by 365.
* Revenue is calculated o basis of price per night. It is assumed the security deposit is returned to the  customer once         they checkout and the cleaning fees is spent in cleaning the property.
* Number of reviews is considered a positive trait for any property. Higher count of reviews shows more engagement.
* Availability within 30, 60 ,90 and 365 days are considered highly similar(as shown later). Yearly availability is taken       into analysis because tourism is seasonal in nature.


### Derived Key metrics :
For this purpose of getting the top zipcodes there are some key metrics that I'll base my analysis on. Some of these metrics are assumptions whereas the others are researched based on information on property evaluation.

* Reviews: Number of reviews on a property depict a lot about the property. More number of reviews mean the property has been booked more often as compared to properties with fewer number of reviews. A zipcode that comprises of properties with more reviews has high engagement with users and more probable to be booked in future.

* Occupancy Rate: It is the percentage of occupancy of the property in a given month/year. Greater the availability , lesser is the occupancy. More occupancy will A property that is occupied 365 days in a year has a occupancy rate of 100% whereas a property.

* Annual Return: It is the revenue generated from the property on a yearly basis. For the purpose of this analysis, the annual return is calculated by multiplying the price per night, yearly occupancy rate and 365 days - (price/night* yearly_occupancy * 365)

* Rent Ratio: It's the annual rent collected from the property divided by the price of the property. The higher the rent ratio the better. It means either that the property is bought at a cheap rate or the rent is higher. In either of these cases, the investor is at gain.

* Break Even Time: Break-even time represents the amount of time it takes for an investment to make back its original cost. It is calculated by dividing the original cost of the property by annual rent generated by the property. But since the rent for the property will not be same every year, an increase of 10% in the rent generated yearly is considered. So lesser is the break even time, the better it is for the investor since after the break event time, most of the revenue will be a profit for the investor and properties with high break even time will take longer to even out the expenses.



### Key Findings:
* Most of zipcodes in Manhattan and Brooklyn have higher property cost. Since these zipcodes are also popular in terms of tourism they make some excellent choice for investment.

* Price and Availability are not inversely proportional. Customers are not hesitant to pay higher price ahead of time. The company can capitalize this behavior into their pricing scheme.

* Staten Island and Queens Neighbourhood have limited choices but it also gets fewer guests. In case the company wants to diversify, they should pick the top zips from different neighbourhoods to minimize risk.

### Top Zipcodes:
* 11434
* 10003
* 10013
* 11201
* 11217 and 10014

