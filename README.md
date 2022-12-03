#CitiBike Analysis for August 2019 

###Overview
This project is intended to analyze and visualize data from the New York City CitiBike program for the August 2019 time period.  This data was obtained from the CitiBike program website, scrubbed and organized using Pandas (via jupyter notebook) and imported and visualized in Tableau Public.   

Link to data: https://ride.citibikenyc.com/system-data

The analysis of this data and associated visualizations will be discussed in the results and summary sections of this document. 

###Data Process 
The data was downloaded from the Citibike program in a CSV file.  The file contains over 2 million records.  Minimal data scrubbing was needed in order to process the data.  However, a column type change was needed for the trip duration.  In order to change this column from an object into something that was able to be visualized, it was imported into a Pandas DataFrame and using the pandas.to_datetime() function, was converted into the number of minutes for the ride.  Once this conversion was complete, the dataframe was exported into a separate CSV file in order to be linked to the Tableau workspace for visualization. 


###Results
Visualization of the various measures can be found in the Tableau story that is posted on the Tableau Public site. [link to dashboard](https://public.tableau.com/app/profile/kellie.brabec/viz/Week15Challenge-CitiBikeRideAnalysis/RideAnalysis#1)

####Total Number of Rides: 
There were a total of 2,344,224 rides in August 2019. 

####Subscriber vs Customer Breakdown: 
443,865 rides were taken by customers
1,900,359 rides were taken by subscribers 

INSERT LINK TO IMAGE

####Gender Breakdown: 
Unknown: 225,521 
Female: 588,431
Male: 1,530,272 

INSERT LINK TO IMAGE 

####Ride Analysis: 
The majority of rides were under 30 minutes long, with the majority of of those being under 10 minutes. 

INSERT LINK TO IMAGE

####Ride Distribution by Gender:
The majority of all rides were under 15 minutes, regardless of gender.

INSERT LINK TO IMAGE 

####Ride Analysis by Weekday: 
Rides generally occurred during standard commuting hours, Monday through Friday from 6am to 10am, and Monday through Friday from 4pm through 8pm.  There was an outlier on Wednesday evenings, and it is worth doing further analysis to determine why there were substantially less outbound rides during this time period. 
On the weekends, rides were primarily during noncommuting hours, lending support to the theory that these days are more tourist focused or recreational rides.

INSERT LINK TO IMAGE 

####Ride Analysis by Weekday by Gender: 
This view of the data reinforces that the majority of riders are male, and rides are used primarily during commuting hours.  

INSERT LINK TO IMAGE 

####Ride Analysis by Subscriber Type and Gender: 
The primary subscriber demographic is male, with the highest number of rides taken by this group on Thursday afternoons during the commuting period.  

INSERT LINK TO IMAGE 

###Summary and Suggestions 
The program appears to be well received and used by male identifying customers.  It does appear to have a deficit in non-male identifying users, and this could be due to any number of factors, that could be mitigated if they are identified. 

####Gender 

In order to expand the customer base and grow the subscriber base, it is recommended that marketing efforts focus towards demographics that do not identify as male.  This would necessitate a change in how gender is tracked by the CitiBike service.  The 'Unknown' should be expanded to include 'Non-Binary', 'Other', or 'Prefer not to Say' rather than leaving it as 'Unknown'.  This would allow more accurate reporting usage by gender use more inclusive language in reporting and analytics.  

####Cost Savings 

Reporting on the average distance of a ride would be helpful to show current users and potential users the benefit of using the CitiBike service.  A comparison of the cost of the length of a ride on a CitiBike service, to an average rideshare service, taxi, public transportation may convince users to use the service.  Additional measures on time it takes to travel the average distance during peak times may show users that it is more time efficient to utilize the CitiBike service than another method of transportation.  These measurements could also be used to show the environmental impact of CitiBike usage towards more traditional methods of transportation.  

####Usability 

Additionally, analysis should be done to determine if riders are starting and ending at the same location (round trip) or if they pick up a ride at one location, and then turn the bike in, pick up a second bike and go to a second location or return to the first.  This would help determine if rides are commuter rides or if they are rides more focused on tourist/social events or weekend chores.  
