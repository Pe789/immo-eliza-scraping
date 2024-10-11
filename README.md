JUPITER NOTEBOOK TO BE RUN CELL BY CELL SEQUENTIALLY !!! (or run all)


# Immo Eliza - Data Collection

- Repository: `immo-eliza-scraping`
- Type: `Consolidation`
- Duration: `5 days`
- Deadline: `11/10/2024 4:00 PM`
- Team: Solo

## Learning Objectives

Use Python to collect as much data as possible.

At the end of this (sub)project, you will:
- Be able to scrape a website
- Be able to build a dataset from scratch


## The Mission

The real estate company "Immo Eliza" wants to develop a machine learning model to make price predictions on real estate sales in Belgium. They hired you to help with the entire pipeline. [Immoweb](https://www.immoweb.be/nl) is a commonly used website for Belgian properties.

Your first task is to build a dataset that gathers information about at least 10000 properties all over Belgium. This dataset will be used later to train your prediction model.


The final dataset should be a `csv` file with at least the following 18 columns:
- Property ID
- Locality name
- Postal code
- Price
- Type of property (house or apartment)
- Subtype of property (bungalow, chalet, mansion, ...)
- Type of sale (_note_: exclude life sales)   >> NOT IN LIST, BUT EXCLUDED IN THE SEARCH URL
- Number of rooms
- Living area (area in m²)
- Equipped kitchen (0/1)
- Furnished (0/1)
- Open fire (0/1)
- Terrace (area in m² or null if no terrace)
- Garden (area in m² or null if no garden)
- Number of facades
- Swimming pool (0/1)
- State of building (new, to be renovated, ...)

## Must-have features (for the dataset)

- The data should have properties across all Belgium >> SORTING IN INITAL LIST_URL BY "NEWEST : THIS SHOULD GIVE A RANDOM SELECTION ACCROSS BELGIUM
- There should be at minimum unique 10000 data points >> LIST IN IMMOWEB ARE BY DEFAULT LIMITED TO 333 PAGES, EACH OF 30 PROPERTIES.  HENCE INITIAL SET UP IS FOR 9990 DATAPOINTS
								                          A SEPERATE LIST COULD BE RUN FOR "HOUSES" AND "APPARTMENTS" AND COMBINED.  MAKING TO THE TOTAL OF DATAPOINT = 19980.
- Missing information is initially encoded with `None`>> FIELD LEFT BLANK FOR NOW
- Whenever possible, record only numerical values (for example, instead of defining whether the kitchen is equipped using `"Yes"` or `"No"`, use binary values instead)
- Use appropriate and consistent column names for your variables (those will be key to training and understanding your model later on)
- No duplicates >> TO BE CHECKED IN DF
- No empty rows >> TO BE CHECKED IN DF

AS MUCH AS POSSIBLE, RAW DATA WAS RETRIEVED FOR PERFORMANCE REASONS
IN THE NEXT PHASE, DATA ENHANCEMENT BY IMPLEMENTING RULES LIKE: YES =1, NO = 0. Or if number of open fires >= 1, then 1, otherwise 0, etc.

## Tips

- NEXT POSSIBLE ENHANCEMENT TO IMPROVE PERFORMANCE : USE CONCURRENCY (Python advanced, Bonus material)

## Deliverables

1. Publish your source code on a GitHub repository:
    - Make a private repository first (`immo-eliza-scraping`), share it with your team and coaches
      - Make it public at the end of the project
    - Have a `scraper` folder with your Python modules for scraping (note: you can use OOP or functions. Classes are not mandatory for this project. )
    - Have a `data` folder with the dataset - feel free to subdivide the folder (e.g. `raw`, `cleaned`)
    - Have a `README.md` file
    - Have a `main.py` file to run the scraper >> NOT YET IN USE
    - Have a `requirements.txt` file
    - Have a `.gitignore` file

2. Write a convincing and clear README file, including following elements as you see fit:
   - Description
   - Installation
   - Usage
   - Sources
   - Visuals
   - Contributors
   - Timeline

3. We will have project debrief and show and tell on Friday at 4:00 PM. Volunteers or randomly selected people will show their repos.

## Evaluation criteria

| Criteria       | Indicator                                  | Yes/No |
| -------------- | ------------------------------------------ | ------ |
| 1. Is complete | Contains a minimum of 10000 data points    |        |
|                | Contains data across whole Belgium         |        |
|                | The dataset has no empty rows              |        |
|                | There are few non-numeric values           |        |
|                | Your code is slick & clean                 |        |
|                | Repository and commit history is clear     |        |
| 2. Is great    | Used threading/multiprocessing             |        |

## Final note

