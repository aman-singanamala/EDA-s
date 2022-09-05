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
    

<hr>

<h2>Neighbourhood_group</h2>


<ol>
    <li> Brooklyn </li>
    <li> Manhattan </li>
    <li> Queens </li>
    <li> Staten Island </li>
    <li> Bronx</li>
</ol>

```
airbnb['neighbourhood_group'].unique()
sns.countplot(x='neighbourhood_group',data=airbnb)
plt.show()
```
![graph](.//data/neighbourhood_group.png)

<h1> There are more number of Hotels in Manhattan and less in Staten island </h1>


<hr>

<h2>Room type</h2>


<ol>
    <li> Private room </li>
    <li> Entire home/apt </li>
    <li> Shared room</li>
</ol>

```
airbnb['room_type'].unique()
sns.countplot(x='room_type',data=airbnb)
plt.show()
```
![graph](.//data/room_type.png)

<h1> Entire home/apt room types are high and shared room types are ow </h1>


<hr>