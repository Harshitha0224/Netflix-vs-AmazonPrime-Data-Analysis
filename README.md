# Netflix-vs-AmazonPrime-Data-Analysis
Comparative analysis of Netflix and Amazon Prime content across age groups, genres, and content types using Power BI and Python.

# Project Summary

I built this project to analyse and compare the content strategies of Netflix and Amazon Prime Video. My goal was to move beyond simple counts and answer specific business questions about their target audiences, genre focus, and content mix.

I managed the entire data analysis lifecycle, starting with two separate, messy datasets. I used Power BI and Power Query to clean, transform, and model the data. The final deliverable is a 3-page dashboard (screenshots below) that reveals the key strategic differences between these two streaming giants.

🛠️ Tools Used
Power BI: For data modelling, analysis, and interactive dashboard creation.

Power Query (in Power BI): For all data cleaning, transformation, and preparation (ETL).

🧹 Data Cleaning & Transformation (The Hardest Part)
The raw data were unusable for a direct comparison. The cleaning and transformation process was the most critical part of this project.

Standardising Age Ratings: The rating columns were inconsistent (e.g., Netflix's 'TV-MA' vs. Prime's '18+'). I created a new Conditional Column to map all variations into five standardised categories: Adults (25+), Young Adults (18-25), Teens (10-17), Kids (Below 10), and Unrated / Unknown.

Un-pivoting Genres: The listed_in (genre) column had multiple values in one cell (e.g., "Dramas, Thrillers"). I used the "Split Column by Delimiter into New Rows" feature to ensure every genre could be counted accurately.

Fixing Load Errors: The "Split to Rows" step created intended show_id duplicates. I resolved the resulting "one-to-many" error by disabling "Enable load" on the original staging tables and only loading the final, unified Master_Data table into the model.

📊 My Analysis & Findings (Dashboard Screenshots)
My dashboard is broken down into three pages, each answering one of the key questions.

1. Analysis 1: Audience Focus by Age Group
This view shows the overall composition of the content library for each platform.

<img width="1354" height="722" alt="Page1 png" src="https://github.com/user-attachments/assets/fa2688e5-c2aa-4311-ad72-e4729cd8e541" />

Finding: The data shows a clear strategic divergence. The Netflix library is heavily skewed towards Adults (25+) and Young Adults (18-25). In contrast, Prime Video has a more balanced catalogue with a visibly larger share of content dedicated to the Kids (Below 10) market.

2. Analysis 2: Popular Genre Analysis
This page identifies the "niche" genres where each platform dominates.

<img width="1110" height="779" alt="Page2 png" src="https://github.com/user-attachments/assets/c1016027-32c8-4a39-9378-37bf5d86872a" />

Finding: The screenshot above (filtered to a Top N for clarity) shows the overall genre differences. Netflix (red) dominates TV Action & Adventure, while Prime Video (blue) is strong in Arthouse.

Output (Using the Slicer): The real insight comes from using the Age_Group slicer. For example, when filtering for "Kids (Below 10)," the chart completely changes to show "Kids' TV" and "Animation" as the top genres, revealing the specific content focus for that audience.

3. Analysis 3: Content Mix (Movie vs. TV Show) by Age
This was the most significant finding. I analyzed the format of the content (Movie or TV Show) within each age group.

<img width="1105" height="740" alt="Page3 png" src="https://github.com/user-attachments/assets/f6d33502-f55f-4750-975c-ad8c10068154" />

Finding: A clear pattern emerged. For Adults (25+), Young Adults (18-25), and Teens (10-17), the libraries are overwhelmingly composed of Movies.

Key Insight: This strategy completely flips for the Kids (Below 10) audience. For this group, TV Shows make up a much larger portion of the content. This shows a deliberate, shared industry strategy: use films to attract adult audiences, but use TV series to retain kids and families.
