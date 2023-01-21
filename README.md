# Bikesharing

![image](https://user-images.githubusercontent.com/112348240/213840731-05fff15d-bd0d-4a98-87e6-5e45d9276661.png)


# Background

  Now that we've gotten a good idea of how to create our story, there is still some more work to be done to convince investors that a bike-sharing program in Des Moines is a solid business proposal. To solidify the proposal, one of the key stakeholders would like to see a bike trip analysis.

For this analysis, I’ll use Pandas to change the "tripduration" column from an integer to a datetime datatype. Then, using the converted datatype, you’ll create a set of visualizations to:

  - Show the length of time that bikes are checked out for all riders and genders
  - Show the number of bike trips for all riders and genders for each hour of each day of the week
  - Show the number of bike trips for each type of user and gender for each day of the week.
Finally, I’ll add these new visualizations to the two you created in this module for your final presentation and analysis to pitch to investors.

# **Deliverable 1: Change Trip Duration to a Datetime Format**

Using Python and Pandas functions, I’ll convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After I convert the "tripduration" column to a datetime dataytpe, I’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2.

Follow the instructions below to complete **Deliverable 1.**

  1. Download the `NYC_CitiBike_Challenge_starter_code.ipynb` file into your bikesharing folder, and rename it `NYC_Citibike_Challenge.ipynb`.
  
  ![image](https://user-images.githubusercontent.com/112348240/213844698-47c81d8e-305b-4042-a145-80def5fa37ee.png)

  2. Use the instructions below to add code where indicated by the numbered-step comments in the starter code file. We have     provided the dependencies you will need for this challenge.
  
  3. In Step 1, create a DataFrame from the `201908-citibike-tripdata.csv` file.
  
  ![image](https://user-images.githubusercontent.com/112348240/213844773-f2540ce0-fb52-4886-a427-3b1f24eb7cea.png)

  4. In Step 2, check the datatypes of each column in the DataFrame.
  
  ![image](https://user-images.githubusercontent.com/112348240/213844816-5c9b4b98-0a2f-4363-9516-c336356ad630.png)

  5. In Step 3, convert the "tripduration" column to a datetime datatype by passing the DataFrame column and the units inside the `to_datetime()` function.
  
  ![image](https://user-images.githubusercontent.com/112348240/213844863-8d94bad3-a67c-439d-aa95-3e6afa4dbe33.png)

  6. In Step 4, check the datatypes of the DataFrame.
  
  ![image](https://user-images.githubusercontent.com/112348240/213844915-88133879-aed3-4ebc-8f70-f28eb9344b52.png)

  7. Confirm that the converted values in the "tripduration" column match the following image:
  
  ![image](https://user-images.githubusercontent.com/112348240/213845036-438bf738-ae17-490b-89dd-81fcf5249c00.png)

  8. In Step 5, export the DataFrame as a new CSV file without the index column. Use this new CSV file for Deliverable 2.
  
  ![image](https://user-images.githubusercontent.com/112348240/213845087-6ca401b9-4ec8-4155-9162-abcea7b2ffea.png)

# **Deliverable 2: Create Visualizations for the Trip Analysis**

Using Tableau, create visualizations that show:

- How long bikes are checked out for all riders and genders.
- How many trips are taken by the hour for each day of the week, for all riders and genders.
- A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.

Open Tableau and import the new CSV file that contains the conversion of the "tripduration" column to a datetime datatype in a new Tableau workbook.

# Create the Checkout Times for Users Viz# 

  In this visualization, you’ll graph the length of time that bikes are checked out for all riders.

  1. Add the number of records or the generated field that counts the number of records in the CSV file to the Rows.

  2. Add the "tripduration" column you converted to the Columns, and filter the "More" option by "Hour".

  3. Add the "tripduration" column again to the Columns, and filter the "More" option by "Minute", and then change the values from "discrete" to "continuous".
  4. Add the "tripduration" column that shows the "Hour" to the Filters field, and select "Show Filter".

  5. Edit the X and Y axis labels by right-clicking on the axis label and selecting "Edit Axis".

  6. My graph should look similar to the image on the module:
    
![Chckout Times for Users](https://user-images.githubusercontent.com/112348240/213360009-401c55a0-968b-49ec-ac6f-386976d728ea.png)

# Create the Checkout Times by Gender Viz

In this visualization, I’ll graph the length of time that bikes are checked out for each gender.

  1. Repeat steps 1-4 of the "Checkout Times for Users" visualization.

  2. Add the converted column for gender as a color to the Marks field, add it to the Filters field, and select "Show Filter".

  3. Edit the X and Y axis labels by right-clicking on the axis label and selecting "Edit Axis".
  
  4. My graph look similar to the challenge image:

![Checkout Times by Gender](https://user-images.githubusercontent.com/112348240/213360010-8361477a-1354-4382-9326-ca6331e690c2.png)

# Create the Trips by Weekday for Each Hour Viz

In this visualization, you’ll graph the number of bike trips by weekday for each hour of the day as a heatmap.
  1. Add the "Starttime" column to the Rows, and filter the "More" option by "Hour".
  
  2. Add the "Stoptime" column to the Columns, and filter the “More” option by "Weekday".
  
  3. Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.
  
  4. Format the Y axis of the Starttime by Hour to show the 12-hour format, as shown in the following image:
The Format field pane to edit the headers in the chart.

  5. **Optional:** Format the X axis of Stoptime by Weekday as "Abbreviation".
 
 6. My graph looks similar to the challenge  image:
 
 ![Trips by Gender (Weekday per Hour)](https://user-images.githubusercontent.com/112348240/213360011-a1ca0140-a307-4ed3-b9dd-87b9ae7f6946.png)
 
# Create the Trips by Gender (Weekday per Hour) Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour of each day of the week as a heatmap.

Repeat steps 1-3 from the "Trips by Weekday per Hour" visualization.
Add the converted column for "Gender" to the Columns and to the Filters field, and select "Show Filter".
Format the Y axis of the Starttime by Hour to show the 12-hour format.
Optional: Format the X axis of Stoptime by Weekday as "Abbreviation".
Your graph should look similar to the following image:

 ![Trips by Weekday by Hour](https://user-images.githubusercontent.com/112348240/213360013-cff51120-f583-4307-8f38-9d34d2b0eb29.png)

# Create the User Trips by Gender by Weekday Viz

In this visualization, you'll create a heatmap that shows the number of bike trips broken down by gender for each day of the week by each Usertype.

  1. Add the converted column for "Gender" to the Columns and to the Filters field, and select "Show Filter".

  2. Add the "Usertype" to the Rows and to the Filters field, and select "Show Filter".

  3. Add the "Starttime" column to the Rows, and filter the "More" option by "Weekday".

  4. Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.
  
  5. My graph looks similar to the module challenge image:

  ![image](https://user-images.githubusercontent.com/112348240/213604064-7352bd05-8c2e-4e7f-800e-65357902e5a0.png)

# **Deliverable 3: Create a Story and Report for the Final Presentation**

For this part of the Challenge, you’ll create a story in Tableau and write a report that describes the key outcomes of the NYC Citibike analysis you did in the module and in Deliverable 2.

Follow the instructions below to complete Deliverable 2.

In Tableau, create a new Story using visualizations that will support the key findings you want to show.

  1. You must use the five visualizations that you created in Deliverable 2.
  
  ![image](https://user-images.githubusercontent.com/112348240/213846021-09ecd9ef-77b3-4a0f-b17d-e1de09447832.png)
  
  ![image](https://user-images.githubusercontent.com/112348240/213846036-f926ebad-9a04-45e9-88ef-ea39236bbf0f.png)

  ![image](https://user-images.githubusercontent.com/112348240/213846043-37597e47-f47a-424f-ba15-b976f43dad3f.png)

  ![image](https://user-images.githubusercontent.com/112348240/213846066-70a5d6f9-8f37-4de3-9d04-bae7680303d9.png)

  ![image](https://user-images.githubusercontent.com/112348240/213846088-aeab9e70-367d-40f2-a745-98052f62459a.png)

  2. You must use at least two visualizations that you created in this module.

  ![image](https://user-images.githubusercontent.com/112348240/213846104-2d1763db-2af1-4e54-8bc2-01399d33afd9.png)
  
  ![image](https://user-images.githubusercontent.com/112348240/213846117-8c63e46f-a432-480a-8578-a58ad513e0fb.png)


  3. In your README markdown file, include the following:

    - **Overview of the analysis:** Explain the purpose of this analysis.
    We need to convince investors that a bike-sharing program in Des Moines is a solid business proposal

    - **Results:** Using the visualizations you have in your Tableau Story, describe the results of each visualization underneath the image.
      This part is include on my Tableau 

    - **Summary:** Provide a high-level summary of the results and two additional visualizations that you would perform with the given dataset.
      - People that born around 1969 shows in the chart has the highiest group that use the service
      - It was a Total of ** 2,344,224 Rides**
      - it is a total of 1,900,359 Subscriber and 443,865.
      - The group of people by gender that use the most this service are males as they subscribe
      
      Also, there many visualization that could be create with the whole dataset.
      Below is a screenshot of my Dashboard. I create 2 of the but the this is the main one.

![image](https://user-images.githubusercontent.com/112348240/213844139-d1259e61-9138-4886-8825-cbd404c43b8c.png)









[My link to Tableau Public](https://public.tableau.com/app/profile/marisol.gascon.linarez/viz/NYCCitibikeChallenge_16739228347560/NYCCitibikeMainDashboard)

# Sources:

# Module 15 Challenge.
By **Marisol Gascon Linarez**
