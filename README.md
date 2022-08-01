# Bikesharing
In this project, we will use Tableau to present a business proposal for a bike-sharing company from a New York Citi Bike dataset.
[Link to Dashboard](https://public.tableau.com/app/profile/maggie.samaan/viz/BikeSharing_Analysis_16538824219900/NYCCitiBikeStory)

## Background
Last summer, our group of friends went on a trip of a lifetime to New York city for two full weeks, exploring historic landmarks like Central Park, the Statue of Liberty, and the Empire State Building. <br>

It was a magical experience and as we flew home together we looked through our vacation photos and had a realization; one of the key ingredients to the magic was an unlikely suspect, Citi Bike. <br>
We had biked everywhere which allowed you to really get to know the city and interact with the people who live there and who are using bikes for their commutes. 
So, a great idea started to form in our minds. What if we could start a similar bike-share business for our hometown of Des Moines, Iowa. 
And after few weeks of brainstorming we got incredible news that there was a potential angel investor who might be interested in providing seed funding to explore a bike-share program in Des Moines. <br>

This was an exciting prospect, but we know had to think realistically. The mechanics of making this business work might be quite different in Des Moines than in New York City. 

Hence, our first step was to figure out how the bike-share business actually works in New York City. Fom there, we could create a proposal on how it might work in Des Moines. 

### Purpose
Citi Bike data has been released to the public. We intended to use this public data to study the business model of a bikesharing service in a big city like NYC, and how can we make it work in Des Moines. 

## Objectives
1. Change Trip Duration to a Datetime Format
2. Create Visualizations for the Trip Analysis
3. Create a Story and Report for the Final Presentation 

#### The Bigger Picture
1. how many bike trips were recorded during the month of August? 
2. How does ridership grow over time? Find the proportion of short term customers to annual subscribers
3. What are the peak riding hours in the month of August?
4. Create a basic symbol map to visualize the top ten starting locations for bike trips. 
5. Create a basic symbol map to visualize the top ten ending locations for bike trips.
6. What is the gender breakdown of active riders? Create a pie chart to show the gender breakdown of bike riders.
7. What is the average trip duration by age?
8. Which bikes are the most likely due for repair?
9. Create a packed bubbles visualization to represent the variablitiy in bike utilization. 
10. Build a dashboard to show investors the most important relevant data that will support the Des Moines bike-sharing business.
11. Create a story that explains why, given the data, starting a bike sharing company in Des Moines is a good idea. 
12. Change trip duration to datetime format.
13. Create visualizations for the trip analysis:
- How long bikes are checked out for all riders and genders.
- How many trips are taken by the hour for each day of the week, for all riders and genders.
- A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.
14. Create a story and report for the final presentation.


## Resources
- Data Source:
- Software: 
- Libraries and Packages: 
- Online Tools: 

## Resources
Data Source: 201908-citibike-tripdata.csv.zip, NYC_CitiBike_Challenge.ipynb. 
Software: Tableau
Packages & Libraries:
Online Sources: ride.citibikenyc.com/system-data 


## Methods

1. Create a new repository for this module named "bikesharing" and clone the empty repo into your class folder.
2. Download 20198-citibike-tripdata.csv.zip from ride.citibikenyc.com/system-data.
-- For this project, we'll use data from the Citi Bike program in New York City. This data includes a variety of fields, which we'll get to shortly.
-- This zip file contains all the August 2019 data. 
-- We'll use data from August because there is likely more traffic during the summer months. 
3. Tableau is downloaded, open, and ready to go. 
-- Now you need to get some relevant data that you can use to help predict if your bike-share company idea could work in Des Moines. 
-- For this you'll need to turn to your data source: the Citi Bike data.
-- For our analysis, we'll import the CSV file, which contains all the data we'll need this project. 
-- Therefore, we'll technically be working with extract data for our project.
-- Now we can start connecting our data to Tableau so that we can access it. 
-- Let's connect our CSV file. Click "Text file" and then navigate to the location of the Citi Bike data CSV file you downloaded.

4. What questions would you want answered if you were opening a bike-sharing business? Write the questions down.
-- I want to know the age groups that benefit the most from the bike-sharing service, 
-- and use this information to assess the potential market in Des Moines.

1. To answer this question, we need to create a Tableau worksheet that shows the number of trips recorded during our time period. 
-- We won't need a plot; we'll simply display the number of recorded rides.
--- Create a new sheet and rename it to "Number of Trips"
--- Next, go to the left side of the workspace and look at the Measures section. 
--- You should see a measure called 201908-citibike-tripdata.csv (Count). Drag the 201908-citibike-tripdata.csv (Count) measure into the Text box in the Marks section. 
--- You'll see that the worksheet is updated with the number of rides, so that it looks like this: Number of Trips 2,344,224
2. What is the proportion of short-term customers to annual subscribers? Create a pie chart:
--- Create a new sheet called "Customer Type". 
--- for the pie chart, we need the 'usertype' dimension and the '201908-citibike-tripdata.csv (count)' measure. 
---- Within the usertype dimension, you will notice that there are two types of users: subscribers and customers. 
---- "Subscribers" referes to annual subscribers of the bike-saring service, while "customers" are the short-term riders. 
--- Charge the Mark from 'Automatic' to 'Pie'
--- Add the usertype dimension to the "color" mark, 
--- Add the 201908-citibike-tripdata.csv (count) measure to update the wedges of the pie chart to reflect the percentages of custoemr types.
---- drag '201908-citibike-tripdata.csv (count)' measure to the 'Size' mark and the 'Angle' mark 
--- Once these marks are in place, you can place your cursor over the pie wedges to see more details about them. In this case, we can see how many rides were recorded for each type of customer.
3. What are the peak riding hours in the month of August?
-- Create a new worksheet "August Peak Hours".
-- Change the mark type to 'Bar'.
-- In the worksheet, we'll look at the "Starttime" dimension, as this is a good indicator of when customers tend to begin their bike rides. Drag this dimension to the "Rows" section.
-- Since we want to find the peak hours, we need to change "Year" to "Hour" for the Starttime. To do this, click the arrow, scroll down to "More," and select "Hour," 
-- Next, we need to add the 201908-citibike-tripdata.csv (Count) measure. We want the sum of all records, so if Tableau doesn't automatically change it to "SUM," click the arrow and select "Measure (Sum)."
4. Now we're going to use the data to find the most popular stations in the city for starting a bike journey. We'll start by creating a worksheet.
-- Create a new worksheet "Top Starting Locations"
-- A symbol map is a map with symbols that correlate to the numeric value of the map location. 
-- The most popular starting locations will be marked by larger symbols on the map.
-- The measures we'll need for our map are the Start Station Latitude and Start Station Longitude. 
-- These measures will provide the geographic location of the bike rental starting points. 
-- We'll also need the Number of Records dimension.
--- Drag the "Start Station Longitude" measure to the Columns section and "Start Station Latitude" to the Rows section. 
--- Note that you will need to change these to dimensions by clicking the arrow for each item and selecting "Dimension."
--- Note that "Start Station Latitude" and "Start Station Longitude" should not be preceded by "AVG" or "SUM."
-- When the measures are in place, we need to move them over to the Marks section. The type of plot may be set to "Automatic," which should be changed to "Map."
--- Notice that all of the symbols are the same size. 
--- Remember that we want the most popular starting locations, which means we need to adjust the size and color to represent the popularity of a given location.
--- First, we'll adjust the size of the symbols so we can determine the most popular locations at a glance.
--- Drag the 201908-citibike-tripdata.csv (Count) measure into the Size button within the Marks section.
--- We want to adjust the colors to help us differentiate between the most popular locations and less popular locations. 
--- To do this, drag the 201908-citibike-tripdata.csv (Count) measure into the Color mark. 

5. We've created our first symbol map, which will allow us to tell a story with our data later. 
-- Next, let's create a symbol map for the most popular bike ride ending locations.
-- Start by creating a new worksheet and naming it "Top Ending Locations."
-- As we did before, the next step is to identify the dimensions and measures we'll need. 
-- For our geographic coordinates, we want the "End Station Latitude" and "End Station Longitude" measures. 
-- To correspond with our coordinates, we'll need the 201908-citibike-tripdata.csv (Count) dimension as well.
--- Next, drag the "End Station Latitude" to the Rows section and change it to a dimension. 
--- Then drag "End Station Longitude" to the Columns section and change it to a dimension as well.
-- Now we need to add the 201908-citibike-tripdata.csv (Count) measure to the Size mark.
--- The size of the symbols now corresponds to the popularity of a given location, which is exactly what we want
-- Now we just need to add the 201908-citibike-tripdata.csv (Count) to the Color mark. 
--- This will adjust the color of the symbols so that they represent the most popular ending locations. 
--- As before, the darker the color, the more popular the location is.
-- Now, for this worksheet, we're going to change the colors so that we can determine at a glance if a symbol is popular or not. 
--- To do this, first click the Color mark to expand the options, Click "Edit Colors," and then select the palette dropdown. Choose the red-gold color scheme.
--- If the location is more popular, it will be red; if it's less popular, it will be gold. 

6. What is the gender breakdown of active riders?
-- Create a new worksheet and name it "Gender Breakdown." 
-- We'll use this worksheet to create a pie chart for our data to show the gender breakdown.
-- Next, identify the measures and dimensions needed for this worksheet: Gender and 201908-citibike-tripdata.csv (Count) measures.
-- Drag the Gender measure to the Color mark
-- In the Marks section, you'll notice Gender is within a "SUM" function. We'll want to change this to a dimension, as this will allow it to be the sum of all gender rows we have in our data. 
--- Place your cursor over "SUM(Gender)." Click the arrow and select the dimension button.
-- Next, drag the 201908-citibike-tripdata.csv (Count) measure to the Angle mark.
-- If you place your cursor over each piece of the pie, you will see 0, 1, and 2. If you go back to where we downloaded our data, Citi Bike tells us that 0 represents "Unknown," 1 represents "Male," and 2 represents "Female." 
--- But remember, even though we have this information, the audience viewing our data likely will not. Therefore, we need a calculated field.
--- If you place your cursor over each piece of the pie, you will see 0, 1, and 2. If you go back to where we downloaded our data, Citi Bike tells us that 0 represents "Unknown," 1 represents "Male," and 2 represents "Female." But remember, even though we have this information, the audience viewing our data likely will not. Therefore, we need a calculated field.
--- To create a calculated field, locate the Gender dimension in the Data side pane. Click the arrow in the Gender dimension, choose the "Change Data Type" option, then select the "String" option. Note that we need to complete this step to ensure the calculated field works correctly
--- With the data type changed, we can start looking at the calculated field. Click the arrow in the Gender dimension again. This time choose the "Create" option, then select the "Calculated Field" option
--- Change the name of the calculated field to "Number to String."
--- Remember that we want to convert all numbers in the Gender dimension to the string version of unknown, male, or female.
--- if [Gender]= '0' then 'UNKNOWN'
ELSEIF [Gender] = '1' then 'MALE'
ELSEIF [Gender] = '2' then 'FEMALE' END
--- Now return to your worksheet and drag the "Number to String" dimension to the Color mark.
-- Remember that you can place your cursor over each of the pie slices to see which gender tends to use bike sharing the most.

7. What is the average trip duration by age: 
-- Begin by creating a new worksheet named "Average Trip Duration." 
-- The next step is to identify the measures and dimensions needed.
-- we need only the tripduration and birth year. 
-- We'll create an area chart, which will best represent this data. Area charts in Tableau are essentially line charts that are filled in below the line.
-- Get started by dragging the Birth Year dimension into the Columns section, and the Tripduration measure into the Rows section. Be sure to change the Tripduration to be the average rather than the sum.
-- Next, go to the Marks section and change the visualization type to Area:
-- we have a plot that represents our data well. Take a moment to view the worksheet and think about what the data is telling us. How is birth year related to the length of a bike ride?
-- In general, the later the birth year, the longer the ride duration.

8. Which bikes are the most likely due for repair?
-- Begin by creating a worksheet called "Bike Repairs." 
-- Now identify the measures and dimensions needed: Bikeid, Number of Records. 
-- Now let's create a treemap. Start by dragging the 201908-citibike-tripdata.csv (Count) measure to the Size mark.
-- Next, drag the 201908-citibike-tripdata.csv (Count) measure to the Color mark.
-- Finally, drag the Bikeid measure to the Text mark. 
--- You will need to change the Bikeid to a dimension by clicking the arrow in the "Bikeid" box and selecting dimension

-- Consider how this data might be better represented. 
--- Then redesign the worksheet to more clearly represent the bikes that might need the most repairs. 
--- In order to redesign the worksheet, you may need to look at other visualizations that might be a better fit.

9. How variable in bike utilization?
-- Begin by creating a new worksheet named "Bike Utilization".
-- Next, identify the measures and dimensions needed to create the packed bubbles visualization: Tripduration and Bikeid.
-- These will allow us to view the total usage time per bike, as well as which bikes are used the most frequently, which will give us insight into which bikes may need repairs.
-- Go to the dropdown menu in the Marks section and select Circle.
-- Next, drag the Tripduration measure into the Size mark.
-- Then drag the Bikeid into the Text mark.
-- You may notice that the plot doesn't look quite right. There is only one point in the visualization, which is not what we want. 
--- To fix it, change the Bikeid to a dimension.
-- Feel free to change the colors to make the more utilized bikes stand out more.

-- Now that we've got our bike utilization by Bikeid, we can start to piece together some of the questions that we've answered.

10. Build a dashboard to show investors the most important relevant data that will support the Des Moines bike-sharing business.
-- To create a dashboard, click the middle tab (that looks like a grid with a plus sign) at the bottom of your workspace, 
-- Rename the dashboard to "NYC Citi Bike" for now, you can change the name later as the dashboard changes. 
-- Add a title: Start by adding a title to the "NYC Citi Bike" dashboard. We can call it "NYC Citi Bike Dashboard" for now. To do this, click the Floating button.
--- Next, drag the Text object to anywhere on the screen. This will open a window where you can edit the title of the dashboard,
--- Change the size of the title to 16, and move the title to the top left-side of the page.
-- Select worksheets to add: Look through the worksheets you've created so far. Which ones are the most relevant for our audience? 
--- Consider again the data that we want to present and what our audience is most interested in. 
--- Our audience—the investors—want to learn how the Citi Bike program works during the month of August in New York City.
--- First look at the Average Trip Duration worksheet. This worksheet is a good candidate for the primary spot on our dashboard. You will need to select 'Tiled' before we can move forward.
--- Drag Average Trip Duration worksheet to the dashboard:
---- You'll notice that the worksheet is taking up most of the screen, which is not what we want—we want to be able to add other worksheets to the dashboard. To fix this, click the arrow in the top right of the worksheet, and then select "Floating,"
----  This will reduce the size of the worksheet so that you can easily adjust and move it around as you see fit. 
--- When you are adding a worksheet, you can always just select "Tiled" or Floating" first, then drag your worksheet onto the dashboard.
--- Next, we need to identify the total number of rides during the month of August. 
---- We'll use the Number of Trips worksheet for this, so drag the worksheet to your dashboard. Be sure to change it to "floating."
---- You may notice that the font size is relatively small, so let's change it. Return to the worksheet and click the Text button in the Marks section, and then increase the font size so that it's more readable.
---- Go back to the dashboard and adjust the size of the worksheet window. Use your best judgment to reposition it.
--- Next, let's add the Gender Breakdown worksheet by dragging it to the dashboard. Remember to change it to a floating worksheet. 
--- Let's add one more worksheet: Top Starting Location. Drag the worksheet to your dashboard and position it as you see fit.
-- You've created your first dashboard—nice work! There's a lot you can do in a dashboard, so the best way to optimize the design is to keep playing around with the features. Feel free to keep adjusting your dashboard, and remember that yours may not look like your peers' dashboards—and that's okay!

11. Create a story to help our audience understand the bigger picture of NYC bikesharing data:
-- create a new story by clicking the story icon at the bottom of the Tableau workspace.
-- You can drag a worksheet or dashboard into the workspace, and then you can add a caption or comments about the story.
-- As an example, let's drag the Top Starting Locations worksheet into our story,
-- Now you can add a caption or text description. 
--- Text descriptions are used for describing certain parts of the story and should be used to clarify certain outliers in the data, or why certain data makes the most sense. 
--- Let's add text over Manhattan to indicate this area may have more bike rides due to the number of tourists.
--- You've created your first story. Next, let's move on to story points.

-- Story points are simply different points you would like to make about your data. Think of them like the pages in a graphic novel. No image is the same, but they are all part of the larger story.
--- To create a story point, click the Blank button on the Story tab.
--- To create a story point, click the Blank button on the Story tab.
-- Work on finishing the story you want to tell with the data. Add a few more story points to make the story complete.


Data Visualization Process
When creating Tableau stories, or data visualizations in general, there's a general process that should be followed. You can use this process for most visualizations you'll create.

1. Select your questions. During this step, you'll consider which results you want to share with your audience. What do they want to see? How can we use that information to make their decision-making process easier?
2. Execute independent research. You'll need to look at other relevant pieces of information to build a bigger picture. Search other sources to find information that will make your visualization more powerful.
3. Craft your Tableau story. This is when you create your story, primarily from worksheets and other visuals, with descriptions for each of them.
4. Create a written analysis. The written analysis is intended to provide additional insight into what we're trying to convey to our audience. This is a good place to add extra detail so that everyone can get on the same page.
After you've practiced creating Tableau stories, let's create a story for our investors. The purpose of this story is to help them determine whether they should invest in a bike-sharing program in Des Moines.

## Results
1. Total number of bike trips in August is 2,344,224.
2. We create a pie chart to reflect the percentages of customers types using the bike-share service in New York City. 
-- When we hover over the wedges we can see the number of trip recorded for each type of users: 1,900,359 trips for annual subscribers, and 443,865 trips for customers. 
-- This will help us predict the suctomer breakdown in Des Moines and, in turn, propose a business model to investors. 
3. A key piece of data we need is the peak usage hours for the month of August. 
-- This will help us get a better idea of how many bikes we might need in Des Moines, as well as figure out during which parts of the day we'll need the most bikes. 
-- For example, if we need to do maintenance on a bike, knowing the peak usage hours will help us plan for the best time to do that.
-- Based on the bar chart, we found that the top riding hours (the most active time during the day in August) during August in New York city are 5:00 p.m to 7:00 p.m.
-- Based on the data in the bar chart, we suggest bike maintenance be performed between 2:00 a.m. and 5:00 a.m. since this is one o fthe least active riding times,
--- so fewer bikes are needed, which makes it a good time to do maintenance. 
4. Top starting locations symbol map:
5. Top ending locations symbol map: The size and color of the symbols correspond to the popularity of a given location. 
-- The bigger the mark and darker in color, the more popular the location is. 
-- Here, if the location is more popular, it will be red; if it is less popular, it will be gold. 
6. We build a pie chart to represent the gender breakdown of the Citi Bike users in New York City. 
-- We found that men tend to use bike sharing services the most (1,530,272 men, 588,431 female, 225,521 unknown).
7. We create an area chart to visualize the relationship between the birth year and trip duration. 
-- In general, the later the birth year, the  longer the ride duration. 
-- The general trend is that younger riders tend to use the bikes for longer periods of time. 
8. We create a treemap to get an idea of how often each bike is used, and then note which ones are used most frequently. 
-- By hovering over the chart, we can get the Bike ID and number of trips it was used for. 
-- The darker the color of the bike dot the higher the usage of that bike, thus more need for maintenance. 
-- Bikes with the darkest color on the chart have been used for more than 400 trips in NY in the month of August, 2019.
9. We create a packed bubbles visualization using the trip duration and bike ID data. 
-- That will allow us to view the total usage time (in seconddsd) per bike, as well as which bikes are used the most frequently,
--- which will give us insight into which bikes may need repairs. 
-- The bubbles in this plot show the bike utilization levels: if a bike has a higher utilization level, it will be a larger and darker bubble. 
10. Our audience—the investors—want to learn how the Citi Bike program works during the month of August in New York City.
-- 
11. To help the audience understand the bigger picture of the bikesharing business, we create a story in tableau that explains the data from NYC and how we can adapt that business model for Des Moines city in Iowa.


![image](https://user-images.githubusercontent.com/99442686/182068894-ee3628e0-8265-4a51-aa6f-cfd755cefa0e.png)

![image](https://user-images.githubusercontent.com/99442686/182068797-f3ba36e5-7e9f-45a8-9325-bbb64f0b4e8e.png)

![image](https://user-images.githubusercontent.com/99442686/182068856-3b56763f-9ede-46ec-b0a4-c287d4fd5aeb.png)

--- 






















