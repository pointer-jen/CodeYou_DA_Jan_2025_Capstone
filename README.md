  # LEGO
  _A data analysis project designed to exam LEGO data_


  ## Project Setup Instructions

  - Python 3 is required (version 3.12.6 was used)
  - Jupyter Notebook needs to be installed to run "main.ipynb"
  - Clone the repo from github.
  - Setup a virtual environment and activate it.

     | Command | Linux/Mac  | GitBash |
     | ------- | ---------- | ------- |
     | Create | python3 -m venv venv | python -m venv venv |
     | Activate | source venv/bin/activate | source venv/Scripts/activate |
     | Install | pip install -r requirements.txt | pip install -r requirements.txt |
     | Deactivate | deactivate | deactivate |

  - To make sure you have all the necessary packages, run
    "pip install -r requirements.txt".
  - The following packages will be required to run the program:
    - pandas
    - matplotlib
    - SQLite
  - Note: If you want to see more details on cleaning the data you can look at the "data_cleaning.ipynb"


  ## Project Overview
  Use LEGO data to see if there are any noticeable trends by theme.

  ## Project Objective
  Use the data to compare number of pieces to price a break down of number of sets by year, number of sets by theme, and finally average piece cost and list price by theme.


  ## Methods and Rationale
  Method used was to download data sets from Kaggle, then the .csv files were cleaned with python and pandas.  This cleaned data was then exported out to new .csv files.  These cleaned .csv files were then combined and put into sqlite.  With the cleaned combined dataframe matplotlib was used to plot graphs for correlation analysis to help understand any relationships between the values. 


  ## Technologies Used
  
  The project was developed in Jupyter Notebooks with Pandas being used to clean the data sets.  SQLite was used for the database with Matplotlib used for graphs.

  ## Gathering the data

  Data in this project comes from:
  - lego_sets.csv came from https://www.kaggle.com/datasets/mterzolo/lego-sets
  - lego_sets_and_themes.csv came from https://www.kaggle.com/datasets/jkraak/lego-sets-and-themes-database


## Data Dictionary - A description of each variable in the data sets

| Name              | Description                  | Source data set               |
|-------------------|------------------------------|-------------------------------|
| ages              | Age Range of Set             | Lego Sets                     |
| list_price        | Set Price                    | Lego Sets                     |
| num_reviews       | Number of Reviews            | Lego Sets                     |
| piece_count       | Number of Pieces             | Lego Sets                     |
| play_star_rating  | Play Star Rating             | Lego Sets                     |
| prod_desc         | Product Description          | Lego Sets                     |
| set_number        | Set Number                   | Lego Sets                     |
| prod_long_desc    | Product Long Description     | Lego Sets                     |
| review_difficulty | Review Difficulty            | Lego Sets                     |
| star_rating       | Star Rating                  | Lego Sets                     |
| val_star_rating   | Value Star Rating            | Lego Sets                     |
| country           | Country                      | Lego Sets                     |
| piece_cost        | Piece Cost                   | Calculated from Lego Sets     |
| set_name          | Set Name                     | Theme                         |
| year_released     | Year Released                | Theme                         |
| image_url         | Image URL                    | Theme                         |
| theme_name        | Theme Name                   | Theme                         |


## Key Findings
- There is generally a correlation to number of pieces and list price, as more pieces generally results in a higher price.
- There were a suprisingly larger number of sets for 2017 dat set.  This highlighted limitations with the Lego Sets data pulled from Kaggle and was limited to data they scraped from lego.com.  The LEGO Sets & Themes was a larger data set but did not include list price or ratings so was more limited in what could be compared.  I did a quick check using just the data from the cleaned LEGO Sets & Themes data to see sets by year and it gives a fuller picture where 2017 was not a large increase over others but part of a trend up in number of sets per year.
- The star wars them had the biggest numbe rof sets in combined data set (and was the second highest theme in larger data set)
- I was suprised that the average piece cost by theme was not higher for star wars given it's popularity and I thought it would be more expensive due to licensing; however it was not near the top of average piece cost by theme in the combined data set.
- The average list prices being high for the Ultimate Collector Series (UCS) was not surpirsing as man of those are star wars sets but are the higher priced and piece count sets.
- The value star rating compared to start rating seems to trend together for the most part as the star rating increased the value star rating also increased.
- The value star rating compared to review difficulty seemed mostly in line with some outlier exceptions.  Comparing the star rating instead of value star rating to review difficulty did not seem to make much of a difference.
- There seemed to be a trend up in the star rating to year released; however that could be due to limited data set.
- The average piece cost by year released seemed higher for earlier years; however that could be due to limited data set.


