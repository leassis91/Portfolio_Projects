
## <p align="center"> <b> 🏠🚀 INSIGHTS PROJECT - HOUSE ROCKET COMPANY 🚀🏠 </p> </b>

<!-- <img src="https://github.com/leassis91/Portfolio-Projects/blob/master/HouseRocketEDA/houseexample.jpg?raw=true" width=40% height=40% align="center"/> -->

## 💻 About

This is a fictitious case of a real estate purchase and sale company whose purpose is to maximize revenue by taking advantage of the best opportunities in the real estate market.
At the end of the analysis, the project aims to understand the relationship between price and property attributes and then answer some business questions.

This analysis has three main tasks:

- Determine which properties have the best conditions for buying and reselling;
- Create an interactive Dashboard on Heroku, which the company's CEO can analyze the properties by himself;
- Bring business insights from available catalog data.


---

## 1. Business Problem

House Rocket's business model consists of purchasing and reselling properties through a digital platform. The data scientist is responsible for developing an online dashboard to help the CEO company overview properties available on House Rocket's portfolio and find the best business opportunities.<br>


The dashboard must contain:
   * Which properties should the company or not buy.
   * Two criteria analyzed: the first is median price and houses condition, the second is the most suitable season to sell each house.
   * A table with filters where the CEO can view attributes based on the first criteria.
   * A region map view with properties available.
   * A price density map view with the properties' available prices.
   * A table with filters where CEO can view attributes based on the second criteria.
   * The number of recommended properties to buy considering both criteria.
   * Value invested on the purchase of recommended homes considering both criteria.
   * Expected profit considering both criteria.

<br>

## 2. Business Questions

  * Which properties should House Rocket buy?
  * When is the best time to sell a house? At what price?

To answer these questions, we suggested the following:

- Group the data by region:
    - The propertie's region is a variable that greatly influences the price. We have some noble areas and others that aren't the same way, which both affects considerably the price. It would be unfair to compare prices of properties that are not in the same location, to eliminate this influence.

- Group the data by seasons:
    - Each region has its own season attributes, and we are going to rely on them;
 
- Calculate the median of property prices, to eliminate outliers:
    - With the regions and seasons separated, we suggest that properties that are below the median price of each region AND are in **good condition**, can be purchased.

<br>

## 3. Data Wrangling

- This project was taken from the blog <a href="https://sejaumdatascientist.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce">Seja um Data Scientist</a>.
- The dataset is available on [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction).
- Tools used:
  * Python 3.10
    * Packages: Pandas, NumPy, Matplotlib, Seaborn, Geopandas, Folium, Plotly
  * Jupyter Notebook
  * Sublime Text
  * Visual Studio Code
  * Streamlit
  * Heroku Cloud


- Dataset contains house prices for King County, one of 39 counties in the US state of Washington. It includes homes price between May 2014 and May 2015;
- Dataset has 21 columns and 21,613 rows;
- There were several ID's duplicated in the dataset, these were removed;
- There was 1 outlier property with 33 bedrooms that was removed;

* The variables on the original dataset are:<br>

Variable | Definition
------------ | -------------
|id | Identification number of each property|
|date | The date when the property was available|
|price | The price of each property considered as the purchase price |
|bedrooms | Number of bedrooms|
|bathrooms | The number of bathrooms, the value .5 indicates a room with a toilet but no shower. The value .75 or 3/4 bathroom represents a bathroom that contains one sink, one toilet, and either a shower or a bath.|
|sqft_living | Square feet of the houses interior space|
|sqft_lot | Square feet of the houses land space |
|floors | Number of floors|
|waterfront | A dummy variable for whether the house was overlooking the waterfront or not, ‘1’ if the property has a waterfront, ‘0’ if not|
|view | An index from 0 to 4 of how good the view of the property was|
|condition | An index from 1 to 5 on the condition of the houses, 1 indicates worn-out property and 5 excellent|
|grade | An overall grade is given to the housing unit based on the King County grading system. The index from 1 to 13, where 1-3 falls short of building construction and design, 7 has an average level of construction and design, and 11-13 has a high-quality level of construction and design|
|sqft_above | The square feet of the interior housing space that is above ground level|
|sqft_basement | The square feet of the interior housing space that is below ground level|
|yr_built | Built year of the property |
|yr_renovated | Represents the year when the property was renovated. It considers the number ‘0’ to describe the properties never renovated.|
|zipcode | A five-digit code to indicate the area where the property is in|
|lat | Latitude|
|long | Longitude|
|sqft_living15 | The square feet average size of interior housing living space for the closest 15 houses|
|sqft_lot15 | The square feet average size of land lots for the closest 15 houses|

<br>

## 4. Exploratory Data Analysis

![heatmap](https://user-images.githubusercontent.com/67332395/157692872-e8730bd3-1774-4d2a-9cc7-743a5ad7908c.png)




By analysing the heatmap, we can observe the most relevant features that we can focus on the posterior analysis, and then formulate hypothesis to evaluate them as true or false:

  - Hypothesis 1: Properties with waterfront are more expensive, on average;
  - Hypothesis 2: Properties tend to grow its price over the years;
  - Hypothesis 3: Property Price is highly affected by number of bathrooms.

And many others. 

<br>

## 5. Main Insights

1. Properties overlooking the water are on average more expensive (H1 is true);
    * Using the seasonality criterion, we know that certain properties tend to fall its price depending on the season in which they are. We should buy waterfront properties when they are cheaper, and sell in the season that will appreciate the most.
  
2. YoY (Year over Year) property price growth is not relevant (H2 is false);
    * We analysed that the YoY price growth is only 0.18%.

3. We can see down below the high influence of the number of bathrooms in properties price:

![bathrooms-output](https://user-images.githubusercontent.com/67332395/157692544-5e0d9805-0d31-4cb9-b334-8663941ce393.png)

<br>

## 6. Conclusions

  We've concluded that there are 10505 properties that are worth purchasing and reselling them, with a total possible profit of over $ 1 billion dollars ($1,187 million). We also provided an interactive dashboard that can be accessed via browser, either on mobile or computer on [Heroku](https://leassis-houserocket.herokuapp.com).

<br>

## 7. Next Steps

Here are some notes that can be discussed to improve the project in the future:

* We could analyze if is there any advantage to improve the properties condition before being sold to increase the profit.
* We could make a sale price prediction, using Linear Regression Machine Learning, to forecast some another data property prices.
* We could create a telegram bot which provides all information about the house selected, including post-sale profit.

<br>

## 8. References

- Statistics How To - [Interquartile Range](https://www.statisticshowto.com/probability-and-statistics/interquartile-range/#:~:text=The%20interquartile%20range%20(IQR)%20is,of%20that%20interval%20of%20space.&text=If%20you%20want%20to%20know,the%20first%20or%20lower%20quartile.)
- Blog [Seja um Data Scientist](https://sejaumdatascientist.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce/)
- Dataset from [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction)
- Data Information from [Geocenter](https://geodacenter.github.io/data-and-lab/KingCounty-HouseSales2015/)

If you have any other suggestion or question, feel free to contact me via [LinkedIn](https://linkedin.com/in/leandrodestefani)


## 💪 How to contribute

1. Fork the project.
2. Create a new branch with your changes: `git checkout -b my-feature`
3. Save your changes and create a commit message telling you what you did: `git commit -m" feature: My new feature "`
4. Submit your changes: `git push origin my-feature`

---

💡 This "README" file was provided by tgmarinho
https://github.com/tgmarinho/README-ecoleta/blob/master/README.md
