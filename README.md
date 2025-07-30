  # LEGO
  _A data analysis project designed to exam LEGO data_

  I have grown up as a fan of LEGO and have encouraged this with my kid as well.  We enjoy spending time together building with LEGO so I thought it could be a fun topic for my data analysis project for CodeYou.  Bringing together LEGO and data seemed like a good fit.

  ![Lego Data Story Telling Image](https://github.com/pointer-jen/CodeYou_DA_Jan_2025_Capstone/blob/main/images/Lego_data.jpg?raw=true "LEGO Data Project")  _Note: Image was found from google search of Lego data, source of image https://www.linkedin.com/pulse/story-we-create-along-way-value-amber-leah-mcmillan/_ 


  ## Project Setup Instructions

  - Python 3 is required (version 3.12.6 was used)
  - Jupyter Notebook needs to be installed to run "main.ipynb" 
  - Clone the repo from github
  - Setup a virtual environment and activate it

     | Command | Linux/Mac  | GitBash |
     | ------- | ---------- | ------- |
     | Create | python3 -m venv venv | python -m venv venv |
     | Activate | source venv/bin/activate | source venv/Scripts/activate |
     | Install | pip install -r requirements.txt | pip install -r requirements.txt |
     | Deactivate | deactivate | deactivate |

  - To make sure you have all the necessary packages, run
    "pip install -r requirements.txt"
  - The following packages will be required to run the program:
    - pandas
    - matplotlib
    - SQLite
  - Note: If you want to see more details on cleaning the data you can look at the "data_cleaning.ipynb"


  ## Project Overview
  Use LEGO data to see if there are any noticeable trends.

  ## Project Objective
  Use the data to compare number of pieces to price, a break down of number of sets by year, number of sets by theme, as well as average piece cost and list price by theme.


  ## Methods and Rationale
  Method used was to download data sets from Kaggle, then the .csv files were cleaned with python and pandas.  This cleaned data was then exported out to new .csv files.  These cleaned .csv files were then combined and put into sqlite.  With the cleaned combined dataframe matplotlib was used to plot graphs for correlation analysis to help understand any relationships between the values.  In addition I exported the cleaned data to excel files that were then loaded into Tableau Public to provide presentation of project with visuals.


  ## Technologies Used
  
  The project was developed in Jupyter Notebooks with Pandas being used to clean the data sets.  SQLite was used for the database with Matplotlib used for graphs.  Tableau Public was used to create visuals used in story for project presentation.

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
- The star wars them had the biggest number of sets in combined data set (and was the second highest theme in larger data set)
- I was suprised that the average piece cost by theme was not higher for star wars given it's popularity and I thought it would be more expensive due to licensing; however it was not near the top of average piece cost by theme in the combined data set.
- The average list prices being high for the Ultimate Collector Series (UCS) was not surprising as many of those are Star Wars sets but are the higher priced and piece count sets.
- The value star rating compared to star rating seems to trend together for the most part, as the star rating increased the value star rating also increased.
- The value star rating compared to review difficulty seemed mostly in line with some outlier exceptions.  Comparing the star rating instead of value star rating to review difficulty did not seem to make much of a difference.
- There seemed to be a trend up in the star rating to year released; however that could be due to limited data set.
- The average piece cost by year released seemed higher for earlier years; however that could be due to limited data set.

## Project Summary
The primary purpose of the project was to use skills developed through CodeYou along with the LEGO data acquired through Kaggle to see if there are any noticable trends in the data.  This was an exploritory project without a specific problem or question to be solved.  It was instead an exercise in finding, cleaning, and evaluating data.

## Data inconsistencies, limitations, issues
- There were limitations with the LEGO Sets data pulled from Kaggle as it was limited to data they scraped from lego.com
- The LEGO Sets & Themes was a larger data set but did not include list price or ratings so was more limited in what couold be compared.

## Project Presentation
A visual presentation for this project can be found in Tableau Public by going to - [LEGO Data Analysis](https://public.tableau.com/views/CodeYou_DA_Jan_2025_Capstone_Presentation_Jennifer_Pointer/ProjectPresentation?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## Conclusion
From the limited data set you can generally see correlation between number of pieces in a set and the list price.  There was also generally correlation between the value star rating and the star rating.  As a LEGO collector I was suprised that the Star Wars theme sets did not have a higher cost per piece as it seems like they are more expensive so I thought it was perhaps a licensing thing.  However, based on the limited data used this was not the case.  The Ultimate Collector Series (UCS) are more expensive due to the higher piece counts but the price per piece is not higher than other sets.  Overall I found digging into the data to be interesting and if time allows at some point where I could get larger and more recent data sets it could be interesting to see if there are any other trends.  I plan to continue purchasing LEGO but will continue making my purchase decisions based on personal preference and not necessarily value for money or ratings that others have given the set.
