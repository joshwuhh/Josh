Downloaded Dataset from Kaggle for Seattle AirBNB rental history. 
Comprised of three seperate CSV files for Dates of rental, Addresses, and reviews. 
These were all combined into one XLS file and loaded into Tableau
Listings is main table, inner joined with other two by ID = LISTING ID  because everything in listing will be in calendar/reviews by ID  


## Understanding the Data
Most data is not needed for the visualizations such as Name of listing , Comments etc
There are approx. 3.6k locations in Listings 
  1 Million entries in Calendar


Listings - The information on the actual rental (Bedrooms, Location, Price per day, Etc) 
Reviews - Information on reviews for each property. 
     THREE ID's ARE PRESENT. 
      Listing ID : Property Identification from Listing table
      ID : Identification of specific review
      Reviewer ID: Person leaving review 

Calendar - Shows listing, date, Available (true if rented or false if not ), amount rented for 
      

## Use Case  
If someone wanted to start a BNB business, What factors would they need to know? 
1 How expensive is each Zip Code? 
2 What are the best times for him to list it if he chose to also live in the home? 
3 Bedrooms? 
4 Competition? 


## Process 

1. Began by comapring zip to price, changed measure of price to see AVG rather than SUM 
** Ordered this data and see that highest price zipcode is 98134 at $206 AVG **
Adding color to this we now have our first viz, showing clients how much they would be able to charge in each zip. 

We want to now create a map. 
We have lots of location data available but we want to stay consistent. 
We use Zipcode again and apply a map with seperated border lines 
Apply color and verify colors match with our previous bar chart 

This alone doesn't give us information so we add labels in the Marks section for both the zip and drag in average price 
Adjusted size to fit in borders

2. We utilize the date from the Calendar tab and compare it with the SUM price 
We then change the date to weekly to get a better view. 
We see that there is a huge drop off of price in the end of 2016. This is due to lack of data for the following dates. 
This is solved by filtering the data to only show the last day of 2016. 

What can be proved with this visualization is that the begining of the year (Jan - March) is not as successful for rentals. 
Recomendded that the client focus rental periods in the summer (May - July) and Winter (November - December) 

3. Bedrooms? 

Typically the larger the house, the more bedrooms, the higher the cost. 
So we drag in bedrooms from Listings and see that as a value, it doesn't help as much because there are only 8 distinct numerical values.
We change this so it is shown as measure names instead of values. 
To do this we convert it to a dimension with the drop down 
We use the AVG Price again and exclude the NULL value for bedrooms 
Applied price label and ensured it is also SUM 

What can be understood from this data now is that if the client wants to buy a house for an AirBNB the highest price he can charge will be the 6 BR 

4. Competition? 
How many rentals would he be competing against should he choose to buy a property? We begin by using the bedroom dimension again without NULL values
Then we utilize ID as every ID is connected to one property. 
This is changed to a Measure (Distinct CNT) so we know how many listings of that particular bedroom count there are. 
The table we have now shows us that as room count goes up, competition. 
6 Bedrooms go for highest price and entering a property into the rental market creates about a 20% market share in Seattle. (5 competitors) 



## Dashboard 
Utilizing all of the charts created, we make a dashboard that will allow the user to get an insight into the most profitable property type, month 
and area which they can use to make informed decisions when starting or growing their AirBnB rental business in Seattle. 





