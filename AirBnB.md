```python
import pandas as pd
```


```python
review_dict = pd.read_csv('Reviews_data_dictionary.csv')
print(review_dict)
```

             Field  Description
    0   listing_id   Listing ID
    1    review_id    Review ID
    2         date  Review date
    3  reviewer_id  Reviewer ID
    


```python
review = pd.read_csv('Reviews.csv')
```


```python
review.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>listing_id</th>
      <th>review_id</th>
      <th>date</th>
      <th>reviewer_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>11798</td>
      <td>330265172</td>
      <td>2018-09-30</td>
      <td>11863072</td>
    </tr>
    <tr>
      <th>1</th>
      <td>15383</td>
      <td>330103585</td>
      <td>2018-09-30</td>
      <td>39147453</td>
    </tr>
    <tr>
      <th>2</th>
      <td>16455</td>
      <td>329985788</td>
      <td>2018-09-30</td>
      <td>1125378</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17919</td>
      <td>330016899</td>
      <td>2018-09-30</td>
      <td>172717984</td>
    </tr>
    <tr>
      <th>4</th>
      <td>26827</td>
      <td>329995638</td>
      <td>2018-09-30</td>
      <td>17542859</td>
    </tr>
  </tbody>
</table>
</div>




```python
listing_data = pd.read_csv('Listings_data_dictionary.csv')
```


```python
listing_data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>listing_id</td>
      <td>Listing ID</td>
    </tr>
    <tr>
      <th>1</th>
      <td>name</td>
      <td>Listing Name</td>
    </tr>
    <tr>
      <th>2</th>
      <td>host_id</td>
      <td>Host ID</td>
    </tr>
    <tr>
      <th>3</th>
      <td>host_since</td>
      <td>Date the Host joined Airbnb</td>
    </tr>
    <tr>
      <th>4</th>
      <td>host_location</td>
      <td>Location where the Host is based</td>
    </tr>
    <tr>
      <th>5</th>
      <td>host_response_time</td>
      <td>Estimate of how long the Host takes to respond</td>
    </tr>
    <tr>
      <th>6</th>
      <td>host_response_rate</td>
      <td>Percentage of times the Host responds</td>
    </tr>
    <tr>
      <th>7</th>
      <td>host_acceptance_rate</td>
      <td>Percentage of times the Host accepts a booking...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>host_is_superhost</td>
      <td>Binary field to determine if the Host is a Sup...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>host_total_listings_count</td>
      <td>Total listings the Host has in Airbnb</td>
    </tr>
    <tr>
      <th>10</th>
      <td>host_has_profile_pic</td>
      <td>Binary field to determine if the Host has a pr...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>host_identity_verified</td>
      <td>Binary field to determine if the Host has a ve...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>neighbourhood</td>
      <td>Neighborhood the Listing is in</td>
    </tr>
    <tr>
      <th>13</th>
      <td>district</td>
      <td>District the Listing is in</td>
    </tr>
    <tr>
      <th>14</th>
      <td>city</td>
      <td>City the Listing is in</td>
    </tr>
    <tr>
      <th>15</th>
      <td>latitude</td>
      <td>Listing's latitude</td>
    </tr>
    <tr>
      <th>16</th>
      <td>longitude</td>
      <td>Listing's longitude</td>
    </tr>
    <tr>
      <th>17</th>
      <td>property_type</td>
      <td>Type of property for the Listing</td>
    </tr>
    <tr>
      <th>18</th>
      <td>room_type</td>
      <td>Type of room type in Airbnb for the Listing</td>
    </tr>
    <tr>
      <th>19</th>
      <td>accommodates</td>
      <td>Guests the Listing accomodates</td>
    </tr>
    <tr>
      <th>20</th>
      <td>bedrooms</td>
      <td>Bedrooms in the Listing</td>
    </tr>
    <tr>
      <th>21</th>
      <td>amenities</td>
      <td>Amenities the Listing includes</td>
    </tr>
    <tr>
      <th>22</th>
      <td>price</td>
      <td>Listing price (in each country's currency)</td>
    </tr>
    <tr>
      <th>23</th>
      <td>minimum_nights</td>
      <td>Minimum nights per booking</td>
    </tr>
    <tr>
      <th>24</th>
      <td>maximum_nights</td>
      <td>Maximum nights per booking</td>
    </tr>
    <tr>
      <th>25</th>
      <td>review_scores_rating</td>
      <td>Listing's overall rating (out of 100)</td>
    </tr>
    <tr>
      <th>26</th>
      <td>review_scores_accuracy</td>
      <td>Listing's accuracy score based on what's promo...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>review_scores_cleanliness</td>
      <td>Listing's cleanliness score (out of 10)</td>
    </tr>
    <tr>
      <th>28</th>
      <td>review_scores_checkin</td>
      <td>Listing's check-in experience score (out of 10)</td>
    </tr>
    <tr>
      <th>29</th>
      <td>review_scores_communication</td>
      <td>Listing's communication with the Host score (o...</td>
    </tr>
    <tr>
      <th>30</th>
      <td>review_scores_location</td>
      <td>Listing's location score within the city (out ...</td>
    </tr>
    <tr>
      <th>31</th>
      <td>review_scores_value</td>
      <td>Listing's value score relative to its price (o...</td>
    </tr>
    <tr>
      <th>32</th>
      <td>instant_bookable</td>
      <td>Binary field to determine if the Listing can b...</td>
    </tr>
  </tbody>
</table>
</div>




```python
listing = pd.read_csv('Listings.csv',encoding = "ISO-8859-1",low_memory=False)
```


```python
listing.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>listing_id</th>
      <th>name</th>
      <th>host_id</th>
      <th>host_since</th>
      <th>host_location</th>
      <th>host_response_time</th>
      <th>host_response_rate</th>
      <th>host_acceptance_rate</th>
      <th>host_is_superhost</th>
      <th>host_total_listings_count</th>
      <th>...</th>
      <th>minimum_nights</th>
      <th>maximum_nights</th>
      <th>review_scores_rating</th>
      <th>review_scores_accuracy</th>
      <th>review_scores_cleanliness</th>
      <th>review_scores_checkin</th>
      <th>review_scores_communication</th>
      <th>review_scores_location</th>
      <th>review_scores_value</th>
      <th>instant_bookable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>281420</td>
      <td>Beautiful Flat in le Village Montmartre, Paris</td>
      <td>1466919</td>
      <td>2011-12-03</td>
      <td>Paris, Ile-de-France, France</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>f</td>
      <td>1.0</td>
      <td>...</td>
      <td>2</td>
      <td>1125</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>f</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3705183</td>
      <td>39 mÃÂ² Paris (Sacre CÃâur)</td>
      <td>10328771</td>
      <td>2013-11-29</td>
      <td>Paris, Ile-de-France, France</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>f</td>
      <td>1.0</td>
      <td>...</td>
      <td>2</td>
      <td>1125</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>f</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4082273</td>
      <td>Lovely apartment with Terrace, 60m2</td>
      <td>19252768</td>
      <td>2014-07-31</td>
      <td>Paris, Ile-de-France, France</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>f</td>
      <td>1.0</td>
      <td>...</td>
      <td>2</td>
      <td>1125</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>f</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4797344</td>
      <td>Cosy studio (close to Eiffel tower)</td>
      <td>10668311</td>
      <td>2013-12-17</td>
      <td>Paris, Ile-de-France, France</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>f</td>
      <td>1.0</td>
      <td>...</td>
      <td>2</td>
      <td>1125</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>f</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4823489</td>
      <td>Close to Eiffel Tower - Beautiful flat : 2 rooms</td>
      <td>24837558</td>
      <td>2014-12-14</td>
      <td>Paris, Ile-de-France, France</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>f</td>
      <td>1.0</td>
      <td>...</td>
      <td>2</td>
      <td>1125</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>10.0</td>
      <td>f</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 33 columns</p>
</div>




```python
listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 279712 entries, 0 to 279711
    Data columns (total 33 columns):
     #   Column                       Non-Null Count   Dtype  
    ---  ------                       --------------   -----  
     0   listing_id                   279712 non-null  int64  
     1   name                         279537 non-null  object 
     2   host_id                      279712 non-null  int64  
     3   host_since                   279547 non-null  object 
     4   host_location                278872 non-null  object 
     5   host_response_time           150930 non-null  object 
     6   host_response_rate           150930 non-null  float64
     7   host_acceptance_rate         166625 non-null  float64
     8   host_is_superhost            279547 non-null  object 
     9   host_total_listings_count    279547 non-null  float64
     10  host_has_profile_pic         279547 non-null  object 
     11  host_identity_verified       279547 non-null  object 
     12  neighbourhood                279712 non-null  object 
     13  district                     37012 non-null   object 
     14  city                         279712 non-null  object 
     15  latitude                     279712 non-null  float64
     16  longitude                    279712 non-null  float64
     17  property_type                279712 non-null  object 
     18  room_type                    279712 non-null  object 
     19  accommodates                 279712 non-null  int64  
     20  bedrooms                     250277 non-null  float64
     21  amenities                    279712 non-null  object 
     22  price                        279712 non-null  int64  
     23  minimum_nights               279712 non-null  int64  
     24  maximum_nights               279712 non-null  int64  
     25  review_scores_rating         188307 non-null  float64
     26  review_scores_accuracy       187999 non-null  float64
     27  review_scores_cleanliness    188047 non-null  float64
     28  review_scores_checkin        187941 non-null  float64
     29  review_scores_communication  188025 non-null  float64
     30  review_scores_location       187937 non-null  float64
     31  review_scores_value          187927 non-null  float64
     32  instant_bookable             279712 non-null  object 
    dtypes: float64(13), int64(6), object(14)
    memory usage: 70.4+ MB
    


```python
listing["host_since"] = pd.to_datetime(listing["host_since"])
```


```python
listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 279712 entries, 0 to 279711
    Data columns (total 33 columns):
     #   Column                       Non-Null Count   Dtype         
    ---  ------                       --------------   -----         
     0   listing_id                   279712 non-null  int64         
     1   name                         279537 non-null  object        
     2   host_id                      279712 non-null  int64         
     3   host_since                   279547 non-null  datetime64[ns]
     4   host_location                278872 non-null  object        
     5   host_response_time           150930 non-null  object        
     6   host_response_rate           150930 non-null  float64       
     7   host_acceptance_rate         166625 non-null  float64       
     8   host_is_superhost            279547 non-null  object        
     9   host_total_listings_count    279547 non-null  float64       
     10  host_has_profile_pic         279547 non-null  object        
     11  host_identity_verified       279547 non-null  object        
     12  neighbourhood                279712 non-null  object        
     13  district                     37012 non-null   object        
     14  city                         279712 non-null  object        
     15  latitude                     279712 non-null  float64       
     16  longitude                    279712 non-null  float64       
     17  property_type                279712 non-null  object        
     18  room_type                    279712 non-null  object        
     19  accommodates                 279712 non-null  int64         
     20  bedrooms                     250277 non-null  float64       
     21  amenities                    279712 non-null  object        
     22  price                        279712 non-null  int64         
     23  minimum_nights               279712 non-null  int64         
     24  maximum_nights               279712 non-null  int64         
     25  review_scores_rating         188307 non-null  float64       
     26  review_scores_accuracy       187999 non-null  float64       
     27  review_scores_cleanliness    188047 non-null  float64       
     28  review_scores_checkin        187941 non-null  float64       
     29  review_scores_communication  188025 non-null  float64       
     30  review_scores_location       187937 non-null  float64       
     31  review_scores_value          187927 non-null  float64       
     32  instant_bookable             279712 non-null  object        
    dtypes: datetime64[ns](1), float64(13), int64(6), object(13)
    memory usage: 70.4+ MB
    


```python
listing["city"]
```




    0         Paris
    1         Paris
    2         Paris
    3         Paris
    4         Paris
              ...  
    279707    Paris
    279708    Paris
    279709    Paris
    279710    Paris
    279711    Paris
    Name: city, Length: 279712, dtype: object




```python
listing["city"].value_counts()
```




    city
    Paris             64690
    New York          37012
    Sydney            33630
    Rome              27647
    Rio de Janeiro    26615
    Istanbul          24519
    Mexico City       20065
    Bangkok           19361
    Cape Town         19086
    Hong Kong          7087
    Name: count, dtype: int64




```python
paris_listing = listing.query("city=='Paris'")
```


```python
paris_listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 64690 entries, 0 to 279711
    Data columns (total 33 columns):
     #   Column                       Non-Null Count  Dtype         
    ---  ------                       --------------  -----         
     0   listing_id                   64690 non-null  int64         
     1   name                         64627 non-null  object        
     2   host_id                      64690 non-null  int64         
     3   host_since                   64657 non-null  datetime64[ns]
     4   host_location                64522 non-null  object        
     5   host_response_time           23346 non-null  object        
     6   host_response_rate           23346 non-null  float64       
     7   host_acceptance_rate         31919 non-null  float64       
     8   host_is_superhost            64657 non-null  object        
     9   host_total_listings_count    64657 non-null  float64       
     10  host_has_profile_pic         64657 non-null  object        
     11  host_identity_verified       64657 non-null  object        
     12  neighbourhood                64690 non-null  object        
     13  district                     0 non-null      object        
     14  city                         64690 non-null  object        
     15  latitude                     64690 non-null  float64       
     16  longitude                    64690 non-null  float64       
     17  property_type                64690 non-null  object        
     18  room_type                    64690 non-null  object        
     19  accommodates                 64690 non-null  int64         
     20  bedrooms                     51286 non-null  float64       
     21  amenities                    64690 non-null  object        
     22  price                        64690 non-null  int64         
     23  minimum_nights               64690 non-null  int64         
     24  maximum_nights               64690 non-null  int64         
     25  review_scores_rating         48036 non-null  float64       
     26  review_scores_accuracy       47989 non-null  float64       
     27  review_scores_cleanliness    47998 non-null  float64       
     28  review_scores_checkin        47972 non-null  float64       
     29  review_scores_communication  47991 non-null  float64       
     30  review_scores_location       47971 non-null  float64       
     31  review_scores_value          47972 non-null  float64       
     32  instant_bookable             64690 non-null  object        
    dtypes: datetime64[ns](1), float64(13), int64(6), object(13)
    memory usage: 16.8+ MB
    


```python
paris_listing = listing.query("city=='Paris'").loc[:,["host_since","neighbourhood","city","accommodates","price"]]
```


```python
paris_listing.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>host_since</th>
      <th>neighbourhood</th>
      <th>city</th>
      <th>accommodates</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-12-03</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>2</td>
      <td>53</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2013-11-29</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>2</td>
      <td>120</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014-07-31</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>2</td>
      <td>89</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013-12-17</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>2</td>
      <td>58</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014-12-14</td>
      <td>Passy</td>
      <td>Paris</td>
      <td>2</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 64690 entries, 0 to 279711
    Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype         
    ---  ------         --------------  -----         
     0   host_since     64657 non-null  datetime64[ns]
     1   neighbourhood  64690 non-null  object        
     2   city           64690 non-null  object        
     3   accommodates   64690 non-null  int64         
     4   price          64690 non-null  int64         
    dtypes: datetime64[ns](1), int64(2), object(2)
    memory usage: 3.0+ MB
    


```python
paris_listing.isna().sum()
```




    host_since       33
    neighbourhood     0
    city              0
    accommodates      0
    price             0
    dtype: int64




```python
paris_listing.dropna(how = "any",inplace = True)
```


```python
paris_listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 64657 entries, 0 to 279711
    Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype         
    ---  ------         --------------  -----         
     0   host_since     64657 non-null  datetime64[ns]
     1   neighbourhood  64657 non-null  object        
     2   city           64657 non-null  object        
     3   accommodates   64657 non-null  int64         
     4   price          64657 non-null  int64         
    dtypes: datetime64[ns](1), int64(2), object(2)
    memory usage: 3.0+ MB
    


```python
paris_listing.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>host_since</th>
      <th>accommodates</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>64657</td>
      <td>64657.000000</td>
      <td>64657.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2015-11-01 11:06:05.528867328</td>
      <td>3.037877</td>
      <td>113.104614</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2008-08-30 00:00:00</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2014-03-09 00:00:00</td>
      <td>2.000000</td>
      <td>59.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2015-07-07 00:00:00</td>
      <td>2.000000</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2017-05-29 00:00:00</td>
      <td>4.000000</td>
      <td>120.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2021-02-07 00:00:00</td>
      <td>16.000000</td>
      <td>12000.000000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>NaN</td>
      <td>1.588382</td>
      <td>214.479626</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing.describe(include = "object")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>neighbourhood</th>
      <th>city</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>64657</td>
      <td>64657</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>20</td>
      <td>1</td>
    </tr>
    <tr>
      <th>top</th>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>7232</td>
      <td>64657</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing["accommodates"]==0
```




    0         False
    1         False
    2         False
    3         False
    4         False
              ...  
    279707    False
    279708    False
    279709    False
    279710    False
    279711    False
    Name: accommodates, Length: 64657, dtype: bool




```python
paris_listing[paris_listing["accommodates"]==0]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>host_since</th>
      <th>neighbourhood</th>
      <th>city</th>
      <th>accommodates</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>98209</th>
      <td>2020-07-20</td>
      <td>Pantheon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203257</th>
      <td>2020-02-04</td>
      <td>Batignolles-Monceau</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203258</th>
      <td>2016-10-17</td>
      <td>Opera</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203259</th>
      <td>2020-04-24</td>
      <td>Luxembourg</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203260</th>
      <td>2020-04-24</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203261</th>
      <td>2020-07-15</td>
      <td>Batignolles-Monceau</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203263</th>
      <td>2016-06-07</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203264</th>
      <td>2020-09-08</td>
      <td>Pantheon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203265</th>
      <td>2020-09-21</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203267</th>
      <td>2020-10-29</td>
      <td>Observatoire</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203268</th>
      <td>2020-11-04</td>
      <td>Opera</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>203269</th>
      <td>2020-11-10</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>205561</th>
      <td>2020-10-29</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>205562</th>
      <td>2020-11-05</td>
      <td>Reuilly</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>206501</th>
      <td>2020-09-16</td>
      <td>Opera</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207077</th>
      <td>2019-12-17</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207078</th>
      <td>2020-04-20</td>
      <td>Observatoire</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207079</th>
      <td>2020-04-27</td>
      <td>Pantheon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207080</th>
      <td>2020-08-05</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207081</th>
      <td>2020-09-04</td>
      <td>Passy</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207082</th>
      <td>2020-09-07</td>
      <td>Batignolles-Monceau</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207083</th>
      <td>2020-09-10</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207084</th>
      <td>2020-09-16</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207086</th>
      <td>2020-06-08</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208303</th>
      <td>2020-04-15</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208304</th>
      <td>2020-12-15</td>
      <td>Louvre</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208858</th>
      <td>2020-02-04</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208859</th>
      <td>2020-02-04</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208860</th>
      <td>2020-02-05</td>
      <td>Menilmontant</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208861</th>
      <td>2020-02-04</td>
      <td>Reuilly</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208862</th>
      <td>2020-02-04</td>
      <td>Bourse</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208863</th>
      <td>2020-02-04</td>
      <td>Louvre</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208864</th>
      <td>2020-02-04</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208865</th>
      <td>2020-02-05</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208866</th>
      <td>2020-02-05</td>
      <td>Observatoire</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208867</th>
      <td>2019-10-30</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208868</th>
      <td>2016-10-06</td>
      <td>Bourse</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208869</th>
      <td>2020-04-24</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208870</th>
      <td>2020-05-12</td>
      <td>Popincourt</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208871</th>
      <td>2020-06-02</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208872</th>
      <td>2020-07-15</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208873</th>
      <td>2020-07-23</td>
      <td>Popincourt</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208874</th>
      <td>2020-08-12</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208875</th>
      <td>2020-08-12</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208876</th>
      <td>2020-08-12</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208877</th>
      <td>2020-09-17</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208878</th>
      <td>2020-10-09</td>
      <td>Passy</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208879</th>
      <td>2020-04-15</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208880</th>
      <td>2020-10-21</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208881</th>
      <td>2020-10-22</td>
      <td>Pantheon</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208882</th>
      <td>2020-11-26</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208883</th>
      <td>2020-11-26</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208884</th>
      <td>2020-12-21</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>212834</th>
      <td>2020-02-03</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing[paris_listing["accommodates"]==0].count(axis=0)
```




    host_since       54
    neighbourhood    54
    city             54
    accommodates     54
    price            54
    dtype: int64




```python
paris_listing[paris_listing["price"]==0].count(axis=0)
```




    host_since       62
    neighbourhood    62
    city             62
    accommodates     62
    price            62
    dtype: int64




```python
paris_listing[(paris_listing["price"]==0) & (paris_listing["accommodates"]!=0)]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>host_since</th>
      <th>neighbourhood</th>
      <th>city</th>
      <th>accommodates</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>207075</th>
      <td>2019-07-22</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>207076</th>
      <td>2019-10-31</td>
      <td>Enclos-St-Laurent</td>
      <td>Paris</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208301</th>
      <td>2019-05-27</td>
      <td>Palais-Bourbon</td>
      <td>Paris</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208302</th>
      <td>2019-07-19</td>
      <td>Pantheon</td>
      <td>Paris</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208854</th>
      <td>2016-09-16</td>
      <td>Louvre</td>
      <td>Paris</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208855</th>
      <td>2019-11-06</td>
      <td>Luxembourg</td>
      <td>Paris</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208856</th>
      <td>2019-12-02</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>208857</th>
      <td>2019-12-17</td>
      <td>Opera</td>
      <td>Paris</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing = paris_listing[paris_listing["price"]!=0]
```


```python
paris_listing.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 64595 entries, 0 to 279711
    Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype         
    ---  ------         --------------  -----         
     0   host_since     64595 non-null  datetime64[ns]
     1   neighbourhood  64595 non-null  object        
     2   city           64595 non-null  object        
     3   accommodates   64595 non-null  int64         
     4   price          64595 non-null  int64         
    dtypes: datetime64[ns](1), int64(2), object(2)
    memory usage: 3.0+ MB
    


```python
paris_listing.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>host_since</th>
      <th>neighbourhood</th>
      <th>city</th>
      <th>accommodates</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2011-12-03</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>2</td>
      <td>53</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2013-11-29</td>
      <td>Buttes-Montmartre</td>
      <td>Paris</td>
      <td>2</td>
      <td>120</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014-07-31</td>
      <td>Elysee</td>
      <td>Paris</td>
      <td>2</td>
      <td>89</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013-12-17</td>
      <td>Vaugirard</td>
      <td>Paris</td>
      <td>2</td>
      <td>58</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014-12-14</td>
      <td>Passy</td>
      <td>Paris</td>
      <td>2</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing_neighbourhood = paris_listing.groupby('neighbourhood').agg({'price':"mean"}).sort_values("price",ascending = False).round(2)
```


```python
paris_listing_neighbourhood
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>price</th>
    </tr>
    <tr>
      <th>neighbourhood</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Elysee</th>
      <td>211.37</td>
    </tr>
    <tr>
      <th>Louvre</th>
      <td>175.75</td>
    </tr>
    <tr>
      <th>Passy</th>
      <td>161.29</td>
    </tr>
    <tr>
      <th>Palais-Bourbon</th>
      <td>157.51</td>
    </tr>
    <tr>
      <th>Luxembourg</th>
      <td>155.79</td>
    </tr>
    <tr>
      <th>Bourse</th>
      <td>149.63</td>
    </tr>
    <tr>
      <th>Hotel-de-Ville</th>
      <td>144.52</td>
    </tr>
    <tr>
      <th>Temple</th>
      <td>138.43</td>
    </tr>
    <tr>
      <th>Pantheon</th>
      <td>122.98</td>
    </tr>
    <tr>
      <th>Opera</th>
      <td>119.20</td>
    </tr>
    <tr>
      <th>Vaugirard</th>
      <td>107.09</td>
    </tr>
    <tr>
      <th>Enclos-St-Laurent</th>
      <td>103.12</td>
    </tr>
    <tr>
      <th>Batignolles-Monceau</th>
      <td>102.69</td>
    </tr>
    <tr>
      <th>Observatoire</th>
      <td>102.00</td>
    </tr>
    <tr>
      <th>Gobelins</th>
      <td>98.11</td>
    </tr>
    <tr>
      <th>Popincourt</th>
      <td>90.55</td>
    </tr>
    <tr>
      <th>Reuilly</th>
      <td>89.13</td>
    </tr>
    <tr>
      <th>Buttes-Montmartre</th>
      <td>87.25</td>
    </tr>
    <tr>
      <th>Buttes-Chaumont</th>
      <td>82.69</td>
    </tr>
    <tr>
      <th>Menilmontant</th>
      <td>74.93</td>
    </tr>
  </tbody>
</table>
</div>




```python
parise_Elysee_accommodates = paris_listing.query("neighbourhood=='Elysee'").groupby('accommodates').agg({"price":'mean'}).sort_values("price",ascending = False).round(2)
```


```python
parise_Elysee_accommodates
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>price</th>
    </tr>
    <tr>
      <th>accommodates</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>14</th>
      <td>971.00</td>
    </tr>
    <tr>
      <th>13</th>
      <td>842.50</td>
    </tr>
    <tr>
      <th>11</th>
      <td>805.00</td>
    </tr>
    <tr>
      <th>16</th>
      <td>800.00</td>
    </tr>
    <tr>
      <th>12</th>
      <td>529.62</td>
    </tr>
    <tr>
      <th>10</th>
      <td>500.86</td>
    </tr>
    <tr>
      <th>9</th>
      <td>440.27</td>
    </tr>
    <tr>
      <th>7</th>
      <td>411.54</td>
    </tr>
    <tr>
      <th>8</th>
      <td>405.52</td>
    </tr>
    <tr>
      <th>6</th>
      <td>355.51</td>
    </tr>
    <tr>
      <th>5</th>
      <td>328.82</td>
    </tr>
    <tr>
      <th>4</th>
      <td>212.10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>155.10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>153.88</td>
    </tr>
    <tr>
      <th>1</th>
      <td>79.52</td>
    </tr>
  </tbody>
</table>
</div>




```python
paris_listing["host_since"].nunique()
```




    3854




```python
paris_listing_over_time = paris_listing.set_index("host_since").resample("Y").agg({"neighbourhood":"count","price":"mean"})
```

    C:\Users\Frames\AppData\Local\Temp\ipykernel_5076\3062826406.py:1: FutureWarning: 'Y' is deprecated and will be removed in a future version, please use 'YE' instead.
      paris_listing_over_time = paris_listing.set_index("host_since").resample("Y").agg({"neighbourhood":"count","price":"mean"})
    


```python
paris_listing_over_time
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>neighbourhood</th>
      <th>price</th>
    </tr>
    <tr>
      <th>host_since</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2008-12-31</th>
      <td>4</td>
      <td>77.750000</td>
    </tr>
    <tr>
      <th>2009-12-31</th>
      <td>106</td>
      <td>159.641509</td>
    </tr>
    <tr>
      <th>2010-12-31</th>
      <td>416</td>
      <td>125.031250</td>
    </tr>
    <tr>
      <th>2011-12-31</th>
      <td>1339</td>
      <td>124.828230</td>
    </tr>
    <tr>
      <th>2012-12-31</th>
      <td>4592</td>
      <td>111.578615</td>
    </tr>
    <tr>
      <th>2013-12-31</th>
      <td>8142</td>
      <td>107.096414</td>
    </tr>
    <tr>
      <th>2014-12-31</th>
      <td>10922</td>
      <td>100.253800</td>
    </tr>
    <tr>
      <th>2015-12-31</th>
      <td>12147</td>
      <td>103.646250</td>
    </tr>
    <tr>
      <th>2016-12-31</th>
      <td>8867</td>
      <td>114.211345</td>
    </tr>
    <tr>
      <th>2017-12-31</th>
      <td>4585</td>
      <td>108.658888</td>
    </tr>
    <tr>
      <th>2018-12-31</th>
      <td>4294</td>
      <td>138.209362</td>
    </tr>
    <tr>
      <th>2019-12-31</th>
      <td>5685</td>
      <td>129.962533</td>
    </tr>
    <tr>
      <th>2020-12-31</th>
      <td>3363</td>
      <td>143.517098</td>
    </tr>
    <tr>
      <th>2021-12-31</th>
      <td>133</td>
      <td>93.488722</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
paris_listing_neighbourhood
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>price</th>
    </tr>
    <tr>
      <th>neighbourhood</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Elysee</th>
      <td>211.37</td>
    </tr>
    <tr>
      <th>Louvre</th>
      <td>175.75</td>
    </tr>
    <tr>
      <th>Passy</th>
      <td>161.29</td>
    </tr>
    <tr>
      <th>Palais-Bourbon</th>
      <td>157.51</td>
    </tr>
    <tr>
      <th>Luxembourg</th>
      <td>155.79</td>
    </tr>
    <tr>
      <th>Bourse</th>
      <td>149.63</td>
    </tr>
    <tr>
      <th>Hotel-de-Ville</th>
      <td>144.52</td>
    </tr>
    <tr>
      <th>Temple</th>
      <td>138.43</td>
    </tr>
    <tr>
      <th>Pantheon</th>
      <td>122.98</td>
    </tr>
    <tr>
      <th>Opera</th>
      <td>119.20</td>
    </tr>
    <tr>
      <th>Vaugirard</th>
      <td>107.09</td>
    </tr>
    <tr>
      <th>Enclos-St-Laurent</th>
      <td>103.12</td>
    </tr>
    <tr>
      <th>Batignolles-Monceau</th>
      <td>102.69</td>
    </tr>
    <tr>
      <th>Observatoire</th>
      <td>102.00</td>
    </tr>
    <tr>
      <th>Gobelins</th>
      <td>98.11</td>
    </tr>
    <tr>
      <th>Popincourt</th>
      <td>90.55</td>
    </tr>
    <tr>
      <th>Reuilly</th>
      <td>89.13</td>
    </tr>
    <tr>
      <th>Buttes-Montmartre</th>
      <td>87.25</td>
    </tr>
    <tr>
      <th>Buttes-Chaumont</th>
      <td>82.69</td>
    </tr>
    <tr>
      <th>Menilmontant</th>
      <td>74.93</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize = (12,6))
sns.barplot(data = paris_listing_neighbourhood,
           x = "price",
           y = paris_listing_neighbourhood.index,
           color = "red")
plt.title("Neighbourhood in Paris (Premium Localities at Top)")
plt.xlabel("How Expensive? (Euros)")
plt.ylabel("Prominent Places With AirBnBs")
plt.show()
```


    
![png](output_40_0.png)
    



```python
parise_Elysee_accommodates
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>price</th>
    </tr>
    <tr>
      <th>accommodates</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>14</th>
      <td>971.00</td>
    </tr>
    <tr>
      <th>13</th>
      <td>842.50</td>
    </tr>
    <tr>
      <th>11</th>
      <td>805.00</td>
    </tr>
    <tr>
      <th>16</th>
      <td>800.00</td>
    </tr>
    <tr>
      <th>12</th>
      <td>529.62</td>
    </tr>
    <tr>
      <th>10</th>
      <td>500.86</td>
    </tr>
    <tr>
      <th>9</th>
      <td>440.27</td>
    </tr>
    <tr>
      <th>7</th>
      <td>411.54</td>
    </tr>
    <tr>
      <th>8</th>
      <td>405.52</td>
    </tr>
    <tr>
      <th>6</th>
      <td>355.51</td>
    </tr>
    <tr>
      <th>5</th>
      <td>328.82</td>
    </tr>
    <tr>
      <th>4</th>
      <td>212.10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>155.10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>153.88</td>
    </tr>
    <tr>
      <th>1</th>
      <td>79.52</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure (figsize = (12,8))
sns.barplot(data = parise_Elysee_accommodates,
           x = "price",
           y = parise_Elysee_accommodates.index,
           color = "green",
           orient = "h",
           order = parise_Elysee_accommodates.index)
plt.title("Average Price Of AirBnB In Elysee -- vs -- Number Of People That Can Stay")
plt.xlabel("Average Price (Eoros)")
plt.ylabel("Number Of People That Can Stay")
plt.show()
```


    
![png](output_42_0.png)
    



```python
paris_listing_over_time
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>neighbourhood</th>
      <th>price</th>
    </tr>
    <tr>
      <th>host_since</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2008-12-31</th>
      <td>4</td>
      <td>77.750000</td>
    </tr>
    <tr>
      <th>2009-12-31</th>
      <td>106</td>
      <td>159.641509</td>
    </tr>
    <tr>
      <th>2010-12-31</th>
      <td>416</td>
      <td>125.031250</td>
    </tr>
    <tr>
      <th>2011-12-31</th>
      <td>1339</td>
      <td>124.828230</td>
    </tr>
    <tr>
      <th>2012-12-31</th>
      <td>4592</td>
      <td>111.578615</td>
    </tr>
    <tr>
      <th>2013-12-31</th>
      <td>8142</td>
      <td>107.096414</td>
    </tr>
    <tr>
      <th>2014-12-31</th>
      <td>10922</td>
      <td>100.253800</td>
    </tr>
    <tr>
      <th>2015-12-31</th>
      <td>12147</td>
      <td>103.646250</td>
    </tr>
    <tr>
      <th>2016-12-31</th>
      <td>8867</td>
      <td>114.211345</td>
    </tr>
    <tr>
      <th>2017-12-31</th>
      <td>4585</td>
      <td>108.658888</td>
    </tr>
    <tr>
      <th>2018-12-31</th>
      <td>4294</td>
      <td>138.209362</td>
    </tr>
    <tr>
      <th>2019-12-31</th>
      <td>5685</td>
      <td>129.962533</td>
    </tr>
    <tr>
      <th>2020-12-31</th>
      <td>3363</td>
      <td>143.517098</td>
    </tr>
    <tr>
      <th>2021-12-31</th>
      <td>133</td>
      <td>93.488722</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize = (12,8))
sns.lineplot(data = paris_listing_over_time["neighbourhood"] , color ='blue')
plt.xlabel("Years")
plt.ylabel("Number of AirBnBs Localities")
plt.title("Popularity of AirBnB Over Time")
plt.grid(True)
plt.show()
```


    
![png](output_44_0.png)
    



```python
plt.figure(figsize = (12,8))
sns.lineplot(data = paris_listing_over_time["price"] , color ='red')
plt.xlabel("Years")
plt.ylabel("Average Price")
plt.title("Average Price of AirBnB Over Time")
plt.grid(True)
plt.show()
```


    
![png](output_45_0.png)
    



```python
fig , ax = plt.subplots()
ax.plot(paris_listing_over_time.index,paris_listing_over_time['neighbourhood'], label = "New Host", c = "pink")
ax.set_ylabel("New hosts")
ax2 = ax.twinx()
ax2.plot(paris_listing_over_time.index,paris_listing_over_time["price"],label = "Average Price")
ax2.set_ylim(0)
ax2.set_ylabel("Average price")
ax2.set_title("Regulations Lead to Fewer New Hosts And Higher Prices")
plt.show()
```


    
![png](output_46_0.png)
    



```python

```
