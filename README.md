## Billboard Analysis Dashboard

This Python script uses the Dash framework to create a web-based dashboard for visualizing data from the `final_billboard.csv` file. The dashboard uses Bootstrap for styling and Plotly for creating interactive plots.

## Dependencies

The script uses the following Python libraries:

- `collections`
- `dash`
- `dash_bootstrap_components`
- `dash_bootstrap_templates`
- `sklearn`
- `numpy`
- `pandas`
- `plotly`
- `sankey`

## How it works

The script starts by importing the necessary libraries and initializing a Dash app with a Bootstrap stylesheet.

It then reads in a CSV file named `final_billboard.csv` into a pandas DataFrame. This DataFrame is assumed to contain data about Billboard chart songs, including a 'danceability' score for each song.

The script then initializes a new column in the DataFrame, 'Danceability Score', to 0. This column will be used to categorize songs based on their danceability.

A list of ranges is created to define the categories for danceability. Each range represents a score interval of 0.2, from 0 to 1.

The script then iterates over the DataFrame, and for each song, it checks the 'danceability' score and assigns a category based on the defined ranges.

## Dashboard

The dashboard created by this script provides an interactive way to visualize the trends in music genres over the years. Users can select a start and end year, and the dashboard will display a multi-line chart showing the total number of songs in the top 100 for each primary genre per year within the selected time range. This allows users to see how the popularity of different music genres has changed over time. In addition, the dashboard includes a feature for users to select a song and see a table of songs that are similar to it, based on a KNN algorithm.
