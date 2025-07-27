Netflix Data Analysis Project
Overview
This project performs an in-depth analysis of a Netflix movie dataset to uncover trends and insights about movie releases, genres, popularity, and audience reception. The dataset, sourced from Kaggle (ibadatali/netflix-dataanalysis), contains information about 9,827 movies, including their release dates, genres, popularity scores, vote counts, and vote averages. The analysis is conducted using Python with libraries such as Pandas, Seaborn, and Matplotlib to clean, process, and visualize the data.
The project explores key questions about the dataset, such as the most frequent genres, the relationship between popularity and vote metrics, and trends in movie releases over time. It includes both basic exploratory data analysis (EDA) and advanced analyses to provide a comprehensive understanding of the data.
Project Objectives

Data Cleaning and Preprocessing: Handle data types, remove unnecessary columns, and address missing values or outliers.
Exploratory Data Analysis (EDA): Answer fundamental questions about the dataset, such as the most frequent genres, highest/lowest popularity movies, and peak release years.
Advanced Analysis: Investigate temporal trends, genre popularity over time, correlations between metrics, and top-rated movies by genre.
Data Visualization: Create insightful visualizations to illustrate trends and distributions, including histograms, line plots, and bar plots.

Dataset
The dataset is sourced from Kaggle (ibadatali/netflix-dataanalysis) and contains 9,827 rows and 9 columns. Key columns include:

Title: Movie title
Release_Date: Release date of the movie
Genre: Comma-separated genres
Popularity: Popularity score
Vote_Count: Number of votes
Vote_Average: Average vote score
Overview, Original_Language, Poster_Url: Dropped during preprocessing as they were not used in the analysis

Key Preprocessing Steps

Converted Release_Date to datetime and extracted the year.
Dropped irrelevant columns (Overview, Original_Language, Poster_Url).
Categorized Vote_Average into four groups: "not popular," "below average," "average," and "popular."
Handled comma-separated genres using explode() for analysis.
Addressed missing values by dropping rows with NaNs.

Project Structure
The project is contained in a single Python script: copy_of_netflixdata_analysis.py. The script is organized as follows:

Data Import and Setup:
Imports the dataset using the Kaggle API.
Loads necessary libraries: Pandas, Seaborn, Matplotlib.


Data Cleaning and Preprocessing:
Converts Release_Date to year format.
Drops unnecessary columns.
Categorizes Vote_Average using a custom function.
Splits and explodes the Genre column for analysis.


Exploratory Data Analysis:
Analyzes genre frequency, vote distribution, and popularity metrics.
Identifies movies with the highest and lowest popularity.
Examines the distribution of movie releases by year.


Advanced Analysis:
Temporal analysis of movie releases.
Trends in popularity and genre popularity over time.
Correlation analysis between Popularity and Vote_Count.
Distribution of popularity and vote metrics.
Impact of release year on popularity and vote averages.
Identification of top movies by genre based on vote count.


Data Visualization:
Visualizes genre distribution, vote distribution, and release trends.
Plots correlations and distributions using scatter plots, histograms, and line plots.



Key Findings

Most Frequent Genre: Drama is the most common genre, appearing in over 14% of movies.
Popularity and Voting:
25.5% of movies are categorized as "popular" based on Vote_Average.
Spider-Man: No Way Home has the highest popularity (Action, Adventure, Science Fiction).
The United States, Thread has the lowest popularity (Music, Drama, War, Sci-Fi, History).


Release Trends: 2020 was the peak year for movie releases in the dataset.
Genre Popularity Trends: Drama consistently ranks high in popularity, especially for movies with "average" vote ratings.
Correlation: A weak positive correlation (0.146) exists between Popularity and Vote_Count.
Temporal Trends: Movie releases increased steadily from the 1960s, peaking in 2020. Average popularity and vote counts show fluctuations over time.

Dependencies
To run the project, ensure the following Python libraries are installed:

pandas
seaborn
matplotlib
kagglehub (for dataset access)

You can install them using pip:
pip install pandas seaborn matplotlib kagglehub

Additionally, a Kaggle account and API token are required to download the dataset. Follow these steps:

Install the Kaggle CLI: pip install kaggle
Set up your Kaggle API token by placing kaggle.json in ~/.kaggle/ (see Kaggle API documentation).
Run the script to authenticate and download the dataset.

How to Run

Clone this repository:git clone https://github.com/<your-username>/<your-repo-name>.git


Navigate to the project directory:cd <your-repo-name>


Ensure dependencies are installed (see above).
Run the Python script:python copy_of_netflixdata_analysis.py


The script will download the dataset (if not already cached), process it, and generate visualizations and outputs.

Visualizations
The project generates the following visualizations:

Genre Distribution: Bar plot showing the frequency of each genre.
Vote Distribution: Bar plot of Vote_Average categories.
Release Trends: Line plot of movie releases over time.
Popularity Trends: Line plot of average popularity movies over time.
Genre Popularity Trends: Line plot of top genres' popularity over time.
Correlation Analysis: Scatter plot of Popularity vs. Vote_Count, colored by Vote_Average.
Distribution of Metrics: Histograms of Popularity and Vote_Count by Vote_Average.
Impact of Release Year: Line plots of average Popularity and Vote_Count by year.
Most Popular Genres by Year: Bar plot of the most frequent genre per year.

Future Improvements

Incorporate additional datasets to compare Netflix trends with other platforms.
Add statistical tests to validate correlations and trends.
Explore machine learning models to predict movie popularity based on genre and release year.
Enhance visualizations with interactive dashboards using Plotly or Dash.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Dataset provided by ibadatali on Kaggle.
Built with Python, Pandas, Seaborn, and Matplotlib.

Contact
For questions or contributions, please open an issue or pull request on this repository.
