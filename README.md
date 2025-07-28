  # LEGO
  _A data analysis project designed to exam LEGO data_


  ## Project Setup Instructions

  - Python 3 is required.
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


