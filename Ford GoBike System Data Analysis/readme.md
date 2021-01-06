# Ford GoBike System Data Analysis
## by Amira Hagag


## Dataset

> In this project we collect data from bike sharing system used across different cities which are ("San Fransisco, New York and Boston ("Boston / Brookline / Cambridge / Somerville, MA" we abreviated here as "Boston" to be easily investigate), This data set includes information about individual rides made in a bike-sharing system covering the previously mentioned cities.
> The dataset after cleaning contains 1198372 trips with 16 features which are (duration_min, start_station_name, end_station_name, bike_id, user_type, member_age, member_gender, city, start_date, end_date, start_day_of_Week, end_day_of_Week, start_day_Week_type, end_day_Week_type, start_hour and end_hour)

>The cleaning points done before exploration:
>1. Merging the 3 files for the three cities in one dataframe.
>2. Convert start_time and end_time columns to datetime.
>3. Convert member_gender , user_type and city to category.
>4. Drop None values.
>5. Drop the rows that have birth year abnormal value (below 1900).
>6. Drop columns that will not needed ( start_station_id, start_station_latitude, start_station_longitude, end_station_id, end_station_latitude , end_station_longitude).
>7. convert bike_id type to string.
>8. Convert member_birth_year type to int then reconstruct it to age by subtract its value from 2019.
>9. Adjust values for member_gender to be (Male, Female and Other).
>10. Convert duration to minute instead of sec and remove the abnormal values (above one day duration)
>11. Replace start_time and end_time column with 8 columns (start_date : the date at which the trip start, end_date : the date at which the trip end, start_day_of_Week : the day of the week at which the trip start (Saterday, Sunday, Monday, Tuesday, Wednesday, Thursday and Friday), end_day_of_Week : the day of the week at which the trip end (Saterday, Sunday, Monday, Tuesday, Wednesday, Thursday and Friday), start_day_Week_type : the day type of the week at which the trip start (take value week_end for Saterday, Sunday and value week_Day for Monday, Tuesday, Wednesday, Thursday and Friday), end_day_Week_type : the day type of the week at which the trip end (take value week_end for Saterday, Sunday and value week_Day for Monday, Tuesday, Wednesday, Thursday and Friday), start_hour : the hour at which the trip start in 24 format, end_hour : the hour at which the trip end in 24 format)




## Summary of Findings

> Most of the trips has low duration (less than 100 minute), The distribuation for the trips with duration less than 100 minutes is almost symmetric with peak value at 10 minute.
> Most of the ages between 20 and 80 years old, With peak value at age 30 the number of trips reach around 240k trip. There is astarnge jump in the graph of age in age 50.
> The number of trips in New York City is very large compared to the number of trips in San Fransisco or Boston.
> Most of the users are subscribers as the subscribers number of trips exceeds 1 million with (94.2 %) from all trips.
> Most of the users are males as the males number of trips exceeds 900k with (74.52 %) from all trips, while the females not exceed 300k with (21.74 %) and Others are 3.73%, This is alittle bit strange as percentage of males around 3.5 times percentage of females.
> The Pershing Square North station is the Station that has the largest no of trips start from and also the largest no of trips ending at, We also found that most of the stations in the highest no of trips start at also at the highest no of trips end at like W 21 St & 6 Ave station.
> The distribuation of number of trips for the start date mostly like the distribuation of number of trips for the end date, some days have number of large no of trips around the double values of other days.
> The distribuation of number of trips for the start hour mostly like the distribuation of number of trips for the end hour. The peak values for the start hour and end hour around 8-9 AM and 5-6 PM and this is normal because this is the time people go to work and get back to home.
> The Distribution of trips over the week days is normal the different between days not too much except for week end days (saturday and sunday) is less than the work days.
> The Distribution for the trips over the week day type start and end almost the same. The number of trips for week days around 900k (with percentage 78.55 %) which is larger than number of trips for week end around 250k (with percentage around 21.45 %), given that the no of week days 5 and no of week end days 2 it will still week day larger than week end.
> The coorelation map shows that there is a strong coorelation between start_hour and end_hour.
> The customer user type trip duration larger than the subscriber, The females trip duration slightly larger than males, The People in poston spend more on trip than the people in New York than the people in San Fransisco.
> The customers age is slightly larger than subscribers, The males and female age approximatly the same or males slightly large. The people in New York is older than people in San Fransisco older than people in Boston.
> The number of trips for the user type not affected by the other values like gender and city , it showed same distribution which is the value for subscriber is so high with respect to the value for the customer with any city or gender.
> The gender also not affected by othe values, it also showed large value for males with respect to females for any user type or city.
> The value for city also the same like the other two categorical values not affected by the other feature and shwed large number for New York with respect to San Fransisco and Boston with any user type or gender.
> The distribution for end hour and start hour shows that the peak hour for the week end different from the peak hour in the week days, for the week days the peak hours 8-9 AM and 5-6 PM and for the week end days from 1 PM and 3PM.
> All start and end stations with the 20 highest number of trips in the New York City except san francisco caltrain station 2 in the end stations in the San Fransisco city.
> The Distribution of age with respect to duration shows that the duration increase with age increase till age 30 which is the peak then the duration decrease as the age increase and as we found previous there is jump in graph at age 50.
> The start and end hour affected by the type of user, it provides more details that the peak hour for subscriber different from the peak hour in the customer, for the subscriber the peak hours 8-9 AM and 5-6 PM and for the customer from 3 PM and 5PM.
> The Distribution for the start and end date are same and didn't affect by other features like user type, gender and city.
> The female customers spend more time in the trip than female subscribers and the same for males.
> The Customers in New York spend more time than the customers in Boston than the customers in San Fransisco, but for the subscribers the duration is almost the same for all members regardless the city.
> The female in Boston spend more time in the trip than in New York than in San Fransisco and the same for males.
> The Male subscriber are older than the Male customer and the same for female.
> Customers in New York are older than Subscriber in New York, and so on for other cities. 
> Males are older than female and the city didn't affect that.
> The subscribers are older and the jump in the age-duration graph are mainly from customers with gender other in boston city.
> At week end days people spend more time in trips than the week days with peak hour around 3 PM with trip duration value around 14 minutes.

## Key Insights for Presentation

> Distribution for trips over (Duration / Min , Age, City, User Type, Member Gender).
> The relation between the main features which are (Duration / Min , Age, City, User Type, Member Gender).
> THe relation between trip duration and hour of the day.
