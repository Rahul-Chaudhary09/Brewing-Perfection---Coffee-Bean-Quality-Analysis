# Brewing-Perfection - Coffee-Bean-Quality-Analysis

1)	 Project Overview & Goal (The What):
    •	 The main goal was to transform raw, messy data into actionable insights to understand   coffee quality drivers, identify trends, and support inventory management.
2)	 The Initial Challenge (The Why):
    •	The raw data was disparate and contained significant cleaning challenges. For instance, Altitude was in varied formats like (ranges, different units), Grading Dates had inconsistencies, and Bag Weights needed standardization.            There was no clear way to analyse quality.
3)	My Actions (The How – “My Skills in Action”):
    •	Data Acquisition & Cleaning (Power Query):
      o	I started by importing the raw CSV into Power BI. The first critical step was extensive data cleaning in Power Query.
      o	Specifically, I executed transformations to parse Altitude ranges into usable numerical start/end points, standardize Bag Weight units to kilograms, and ensure all date columns (Grading Date, Expiration) were correctly formatted.
    •	Data Modeling:
      o	After cleaning, I built a star schema-like data model. This involved creating a dedicated Dim_Date table to enable flexible time-based analysis and establishing one-to-many relationships from Dim_Date to both Grading Date and            Expiration in the main data table.
    •	DAX Calculations:
      o	I then used DAX to create several crucial calculated columns. Key Instances include:
        	Midpoint Altitude: To represent altitude ranges as a single numerical value for analysis.
        	Grading Day and Expiration Day: To quantify freshness and age and can have a check of inventory.
        	Expiration Status: A custom categorical column using SWITCH(TRUE()...) logic to segment inventory into actionable groups like ‘Expired’, ‘Soon Expiring’, ‘Moderate Shelf Life’ & ‘Very Good Shelf Life’ which was particularly              challenging to ensure correct range capturing."
    •	Visualization:
      o	Finally, I designed an interactive Power BI report pages with various visuals (line charts, bar charts, scatter plots) to present these insights clearly.
4)	Key Insights & Output (The - So What? - My Findings):
    •	Through the Report, I could reveal:
      o	Top-performing coffee varieties and origins based on average Total Cup Points.
      o	Correlations between different Sensory Drivers and Total Cup Points, indicating potential quality drivers.
      o	The distribution of coffee inventory across different Expiration Status categories, identifying significant coffee lots of expired or soon-to-expire stock.
5)	Impact On Business (The Who Cares?):
    •	These insights would allow a coffee business to:
      o	Optimize sourcing strategies by prioritizing high-quality origins and varieties.
      o	Improve quality control by understanding quality fluctuations by processing method.
      o	Proactively manage inventory, reducing waste and ensuring fresh product sales by identifying and acting on expiring lots.
6)	 Tools Used:
    •	The primary tool used was Power BI Desktop, leveraging Power Query for ETL, DAX for data modeling and calculations, and its visualization capabilities for reporting.
7)	Lessons Learned / Challenges Overcome (My Growth):
    •	A significant learning curve was the SWITCH(TRUE()...) and range logic for Expiration Status with negative numbers to ensure Precise categorization. This project significantly strengthened my data cleaning, modeling, and DAX             problem solving skills.
