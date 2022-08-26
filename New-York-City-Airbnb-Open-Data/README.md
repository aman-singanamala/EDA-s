<hr>
<i><h3>Abstract</h3></i>

<p>Since 2008, guests and hosts have used Airbnb to expand on traveling possibilities and present a more unique, personalized way of experiencing the world. Today, Airbnb became one of a kind service that is used and recognized by the whole world. Data analysis on millions of listings provided through Airbnb is a crucial factor for the company. These millions of listings generate a lot of data - data that can be analyzed and used for security, business decisions, understanding of customers' and providers' (hosts) behavior and performance on the platform, guiding marketing initiatives, implementation of innovative additional services and much more.</p>
<hr>
<i><h3>Data Source</h3></i>
<p>This dataset has around 49,000 observations in it with 16 columns and it is a mix between categorical and numeric values.</p>

<hr>
<br>
<h2>Importing Libraries </h2>

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import matplotlib.image as mpimg
%matplotlib inline
```


<h2> Read the Data and Start Cleaning the Data </h2>
<ol>
    <li>  Read the Data </li>
    <li> Find the Number of Null values present in each column</li>
</ol>

```
airbnb.isnull().sum()
```

![NUll values](.//data/null_values.png)
    

<h3>Look into categorical values </h3>
<li> neighbourhood_group </li>
<li> neighbourhood </li>
<li> room type </li>


<h3>Price vs Room Type </h3>

```
plt.figure(figsize=(20,15))
sns.scatterplot(x='room_type',y='price',data=airbnb)
plt.xlabel("Room Type")
plt.ylabel("Price")
plt.title("Room Type vs Price ",weight='bold')
plt.show()
```

![Price vs Room Type ]('./../data/price_vs_room_type.png)


<h3> Insight </h3>
* From the graph we can notice that the price in Private and Entire romm havethe highest prices
* The shared room price is always lower than $200

![Same]('./../data/price_vs_room_type_NEIGHBOUR.png)

<h3> Insight </h3>
<li> The highest price of Private Room and Entire Home/Apt is in the same area which is Manhattan. </li>
<li>And also brooklyn has very-high prices in Private Room and Entire Home/Apt.</li>
<li> Shared room's Highest price is in the Queens area </li>
<br>
<hr>