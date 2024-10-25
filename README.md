# Airbnb-Analysis
This project showcases a comprehensive analysis of an Airbnb dataset to uncover key business insights and visualise using Tableau.

## Business Problem
Client wants to start an Airbnb business. They want to know where they should buy a property and list it on Airbnb to rent it out. We need to analyse and optimize factors like location, number of bedrooms, the amount of money they can charge, etc to help select the most profitable property.

## Software Used
Tableau Public

## Data Source
[Airbnb Data 2016](https://www.kaggle.com/datasets/hriditabasu/airbnb-data-2016)    

This dataset comprises of:
- Listings: Description of the properties like the unique id, neighbourhood, property type, etc.
- Calender: Lists details like the date and availability.
- Review: Description of the reviews like the date, reviewer name, comment, etc.

## Methodology
Do an inner join on Listings and Calender tables where Id (Listings) = Listing Id (Calender).      
Since we won’t require the Reviews table for our analysis, we can leave it out.

### Visualizations
1. **Price by Zipcode (Sheet 1):**      
   This can help us determine which zipcodes have the costliest listings so buying a property in those zipcodes would enable the client to charge the most.      
   It is visualized as a bar chart sorted in descending order to show the average prices of properties in the respective zipcodes from the highest to the lowest.

   <img width="344" alt="Screenshot 2024-10-26 at 12 57 44 AM" src="https://github.com/user-attachments/assets/0397aa59-b2fb-4867-b0c4-2418c2625bb3">


2. **Price Per Zipcode (Sheet 2):**      
   A map chart to visualize zipcodes and their respective average prices to find the most profitable areas.

   <img width="712" alt="Screenshot 2024-10-26 at 12 58 51 AM" src="https://github.com/user-attachments/assets/7bbe7402-18d5-4db6-82b1-97488814f33f">


3. **Revenue for Year (Sheet 3):**      
   Client also wants to live in the property himself, so he wants to know what the best times would be to list it on Airbnb to rent it out to other people. Hence, we must find out when people are spending the most money on Airbnb.      
We use the Date (Year and then break it out by Week Number) and filter it to only use records until 31st December 2016, and visualize it against the sum of price (Calender).        
Based on this visualization it can be observed that business is slow towards the beginning of the year and perks up during the summer and the holidays so that’s when the property should be rented out.       

<img width="771" alt="Screenshot 2024-10-26 at 12 59 10 AM" src="https://github.com/user-attachments/assets/fd538935-e800-444b-873e-37d4d39e1d2c">


4. **Average Price vs Number of Bedrooms (Sheet 4):**    
   Average price generated based on number of bedrooms in the properties (exclude Null and 0 bedrooms as that’s not helpful to us). It is seen that the properties with a greater number of bedrooms are a much better investment.

   <img width="447" alt="Screenshot 2024-10-26 at 12 59 19 AM" src="https://github.com/user-attachments/assets/db249f06-8a57-4ab9-9ba5-264f6c224d5c">


5. **Number of Bedrooms vs Listings (Sheet 5):**
   Number of listings based on number of bedrooms by visualizing number of bedrooms against the distinct listing ids.       
   It is observed that with increasing number of bedrooms, the number of listings decreases showcasing a downward trend in competition.

   <img width="317" alt="Screenshot 2024-10-26 at 1 00 10 AM" src="https://github.com/user-attachments/assets/8e42fb30-0624-4c1a-806f-22ad94fe4ede">



## Dashboard
All the visualizations are thus combined into the following interactive dashboard:      
[Airbnb Analysis Dashboard](https://public.tableau.com/app/profile/hridita.basu/viz/AirbnbAnalysis_17298809094880/Dashboard1)

## Insights
1. Three of the most profitable areas are in Seattle, Washington with zipcodes 98119, 98121 and 98136 respectively.
2. Business is slow at the beginning of the year therefore it is more profitable to list the property on Airbnb towards the end of the year, especially during the summer and the holidays.
3. The price per night increases with the increase in the number of bedrooms the property has.
4. Greater the number of bedrooms, lesser the number of listings. Therefore, reduced competition. 

## Future Work
Derive more valuable insights by analysing the reviews for the properties as well as by conducting analyses based on other attributes like city, property type, etc.
