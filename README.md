# Fishing on Lake Winipesaukee

<p align="center">
  <img src="https://github.com/aothree/Fishing-Winni-Classification/blob/main/images/img_8002.jpg"/>
</p>

## Introduction

My friend's father Billy has fished on Lake Winipesaukee for over 40 years.  Each day he fished from 2015-2022 he diligently recorded statistics about where he fished, the weather conditions, and his ultimate results.  

This project was started with the hopes of leveraging Streamlit to display Billy's data in an easily digestible dashboard, and give him an idea of where he may have the best success fishing on a given day.  Beyond that, the project aimed to allow the Streamlit application to take new data in to grow the data set over time, thus making the analysis and modeling more robust.  

Link to Streamlit app: [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dancosta154/winnipesaukee_multiregression/main/winni_st.py)

## Summary
After manually inputting the existing data, the data was cleaned and organized in a {Pandas DataFrame/ SQL?}.  A streamlit app was deployed that has four major sections:

* `Show Me My Fish`
Displays all records from the dataframe, or the user can filter records based on Location, Weather Condition, Temperature, and Wind Speed.  Shows table of the data, provides buttons to download `.csv` files, and displays the filtered data in various data visualizations.  

* `Where Should I Fish?`
Takes the data from user inputs and based on these conditions, tells the user which location they should fish at.  This is determined by looking at "fish caught per day" for each location with the given weather conditions.  The highest "fish caught per day" is the app's recommendation.  Lastly, with the click of a button the user can run a Random Forest regression model that will give the user an estimated number of fish that they'll catch based on all past records.

* `Add Fish`
This project started just by using data from the past.  But to make the app more useful and robust over time, we set up a SQL database that will take new records directly from user input on the app.
{SQL database description}

* `How Does My Data Cluster?`
This sections provides two different unsupervised machine learning options to the user.  They can use KMeans or DBScan clustering models which will divide the records into a number of groups, or 'clusters', such that the data points within each cluster are similar, and dissimilar from the data points in the other clusters.  Lastly, the user has the ability to further analyze these clusters by producing a scatter plot, selecting what will be on the X and Y axis' from a drop-down menu of available features.  

## Conclusion and Next Steps
This app can provide valuable information that helps all Lake Winipesaukee fishers gain an edge.  Billy or anyone else who inputs data from a day fishing on the Lake will be making this app stronger and more useful.  

Happy Fishing!


