# Disney_movie_Data_analysis
The goal of this project is to collect, clean, and analyze Disney movie data to uncover trends in production, budgets, and box office performance from the early Disney classics to modern releases.
🕸️**1. Data Scraping (Data Collection)**
The project begins with web scraping data from Wikipedia using Python libraries such as:
requests – for sending HTTP requests to Wikipedia pages
BeautifulSoup (from bs4) – for parsing HTML and extracting movie details
json – for saving structured data

**Key Steps:**
Identify and scrape Wikipedia pages listing Disney movies (e.g., “List of Walt Disney Pictures films”).
Extract structured information for each movie:
Title
Directors
Writers
Based on (source material)
Release date
Runtime
Budget
Box office
Production company
Save the raw scraped data in disney_data.json.

🧹 **2. Data Cleaning**

After scraping, the raw data contained inconsistencies, HTML artifacts, and non-standard formatting.
The cleaning process was performed in multiple stages using pandas and Python string operations.
Key Cleaning Tasks:
Remove extraneous characters such as "[1]", "(United States)", etc.
Normalize lists and nested attributes (convert from mixed strings/lists to structured lists).
Convert currency values like "$2.6 million" → numeric floats (2600000.0).
Parse release dates into proper datetime objects.
Handle missing or ambiguous values (e.g., “Unknown” → NaN).
Save results as disney_data_cleaned.json.

📊 **3. Data Enhancement**

To enable numeric and time-series analysis, the project adds processed fields:
Running time (int) → numeric duration in minutes
Budget (float) → cleaned budget in USD
Box office (float) → cleaned box office in USD
Release dates (datetime) → standardized release date
This enhanced dataset is saved as disney_finel.json and disney_movie_data_final.csv.

🔍 **4. Exploratory Data Analysis (EDA)**

The exploratory phase uses Jupyter Notebook (Toy story 3.ipynb) with pandas, matplotlib, and seaborn to visualize insights.

**Analyses include:**
🎬 Movie counts over time – number of movies produced per decade
💸 Budget vs. Box Office – financial performance trends
🧑‍🎨 Directors and Producers Frequency – most prolific contributors
🌎 Production Company Analysis – how Disney’s production landscape evolved
⏱ Runtime Trends – average length of Disney movies over time

📈 **5. Insights & Results**

From the analysis, some key findings include:
The 1950s–1960s saw steady production with smaller budgets but high ROI.
Budgets dramatically increased in the 1990s–2000s with the rise of Pixal and CGI animation.
Directors like Ben Sharpsteen, Hamilton Luske, and Clyde Geronimi dominated early Disney productions.
Recent releases (post-2010) show a clear trend of blockbuster-scale investments and global box office dominance.

🛠️ **6. Technologies Used**

Category	Tools
Data Collection	requests, BeautifulSoup
Data Processing	pandas, numpy, json
Visualization	matplotlib, seaborn
Environment	Jupyter Notebook
Output	.json, .csv, .pickle formats

📦 **7. Project Files Overview**
File	Description
disney_data.json	Raw scraped data from Wikipedia
disney_data_cleaned.json	Cleaned and normalized dataset
disney_finel.json	Final enriched dataset with numeric and datetime values
disney_movie_data_final.csv	CSV version for analysis
Toy story 3.ipynb	Notebook for data cleaning, EDA, and visualization
requirements.txt	List of Python dependencies
README.md	Documentation of project structure and insights
