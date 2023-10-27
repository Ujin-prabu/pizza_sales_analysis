# Pizza Sales Analysis


### Project Overview

Used a dummy pizza sales data, the data contained different information like toatl number of pizza sold , the different category of pizza sold etc. I analyzed the data in python (jupyter notebook).[Dashboard Preview]![Screenshot (75)](https://github.com/Ujin-prabu/pizza_sales_analysis/assets/116655082/c84fa706-b687-409b-b041-aaa2afb3e07c)




### Data Source

pizza sales data: The primary data set used is pizza_sales.csv


### Tools used 

1) Python for data analysis
2) Tableau for Visualization.[Tableau Dashboard link](https://public.tableau.com/views/PizzaSalesDashboard_16946899613410/Home?:language=en-US&:display_count=n&:origin=viz_share_link)


### EDA(Exploratory Data Analysis)

1) Checked Total revenue, Avg order value , Total pizza sold,Total orders and Avg pizzas per order
2) Analyzed Hourly Trend for Pizzas sold.
3) Analyzed percentage of sales by pizza category.
4) Analyzed percentage of sales by pizza size.
5) Analyzed Top 5 and bottom 5 selling and ordered pizzas.


### Data Analysis

Below is a part of code i used for analysis

~~~ python

Bottom5_pizza_sold_data=data.groupby('pizza_name')['quantity'].sum().nsmallest(5)
print("Bottom5_pizza_sold:",Bottom5_pizza_sold_data)

bottom_5_pizza_sold=Bottom5_pizza_sold_data.reset_index()


sns.barplot(x='pizza_name',y='quantity',data=bottom_5_pizza_sold,hue='pizza_name',palette="deep")
plt.xticks(rotation=45)
plt.xlabel('Pizza Name')
plt.ylabel('quantity')
plt.title('Bottom 5 pizzas sold')
plt.show()
~~~

### Some interesting Findinds From Analysis

1) The Thai chicken pizza generated the most revenue of $43434.25.
2) The Classic Deluxe Pizza was sold the most 2453 quantities were sold.
3) The Brie Carre Pizza generated the least revenue of $11588.50 also it was sold the least quantity of 490.
4) Classic pizza generated 26.9% of overall revenue.
5) Large pizzas generated 45.89% of overall revenue
