<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/paulabondoc/airline-ratings-data-project">
    <!--img src="images/logo.png" alt="Logo" width="80" height="80" -->
  </a>

<h1 align="center">Airline Ratings Data Visualization</h3>
<h3 align="center">Cleaning and visualizing airline ratings dataset.</h3>

  <p align="center">
    <a href="https://public.tableau.com/app/profile/paula.bondoc/viz/Whatisthebestairlineforyourtrip/AirlineReviewsDashboard">View Demo</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#the-dataset">The Dataset</a>
      <ul>
        <li><a href="#cleaning-the-data">Cleaning The Data</a></li>
      </ul>
    </li>
    <li><a href="#visualization">Visualization</a></li>
    <li><a href="#limitations-and-challenges">Limitations And Challenges</a></li>
    <li><a href="#sources">Sources</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>


## About The Project

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

This project is a data cleaning and visualization of an airline reviews and ratings dataset gathered from the airline reviews website, airlinequality.com. It was made because our family was going on a trip, and I was curious to see which airlines were the best for our route. I also wanted to practice my data cleaning skills and get something fun and useful out of initially messy data.

Below we will talk about the data, data cleaning, visualization, and the limitations of this project.


### Built With

* Python (Pandas)
* Jupyter Notebook
* Tableau for visualization
* Excel for some initial cleaning

## The Dataset

This project used the [Airline Reviews dataset][raw-data] which contains over 128k airline reviews and ratings scraped from [airlinequality.com](airlinequality.com). The reviews are from 2001 to 2023. Each entry contains a customer's review and various ratings of an airline, such as cabin service and food, as well as their route.

![Screenshot of raw dataset, with entries of Route column circled in red.][data-screenshot-before]


### Cleaning The Data

The problem, aside from common problems like duplicate and missing data, is that the `Route` column is a single string, like "Moroni to Moheli". What we would like is for it to be separated into origin and destination columns so that we can create a dashboard that lets us visualize airline ratings by origin and destination.

Ultimately, this is our cleaned `Route` column. A Country and State/Province column was added for both Origin and Destination for disambiguation. A lot of State/Province is null but this is fine as it will be handled by Tableau.

![Screenshot of cleaned route data.][cleaned-route-screenshot]

*Note: I chose to keep entries that contained null values for some of the ratings because I wanted to have as much data as we can and because Tableau will handle it automatically during visualization. This might not be the right choice for other purposes.*

For more details on the data cleaning, check out [the data cleaning notebook][data-cleaning-notebook].

## Visualization

I used Tableau to make the interactive visualization. Click [here][Tableau-viz] to try it out for yourself and explore some airlines for your trip!

[![Screenshot of the viz.][product-screenshot]][Tableau-viz]

[![Tooltip of the viz.][viz-tooltip]][Tableau-viz]


## Limitations And Challenges


There are some limitations worth noting.

First, although most of the data of interest was cleaned (94.7%), not all the data were cleaned due to time. There were simply too many different variations and ways that cities and such were misspelled or mistyped. To go through it all would be a great exercise in patience indeed, which I chose not to undertake at the moment. Any advice and suggestions on how to do them better would be greatly appreciated!

For the purposes of "good enough," and since this project is more for fun and learning, I will accept them. Although I do note that the results in the visualization will be a little skewed as a result. A suggestion for the reviews website is to have upfront data validations when customers leave reviews so that we can save hours that are spent on data cleaning like this.

Second, when using the viz and exploring particular routes, you might find that some of them have airlines with only a few reviews (1 or 2). This makes it hard to really conclude things about the quality of that airline for your trip, which limits the usefulness of the viz. (But for fun, it's not so bad.) To try to mitigate this, users can filter by the number of reviews. The bar's thickness also represents how many reviews they have, with thicker bars indicating more reviews.

## Sources

- [128k Airline Reviews][raw-data], Joel Ljungström
- [airlinequality.com](airlinequality.com)

## Contact

<p>

  **Paula Bondoc** <br>
  &nbsp;&nbsp; GitHub: [@paulabondoc](https://github.com/paulabondoc) <br>
  &nbsp;&nbsp; LinkedIn: https://linkedin.com/in/paubondoc

  Project Link: [https://github.com/paulabondoc/airline-ratings-data-project](https://github.com/paulabondoc/airline-ratings-data-project) <br>
  Viz Link : https://public.tableau.com/app/profile/paula.bondoc/viz/Whatisthebestairlineforyourtrip/AirlineReviewsDashboard

</p>



<!-- MARKDOWN LINKS & IMAGES -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/paubondoc
[product-screenshot]: <images/viz screenshot.png>
[viz-tooltip]: images/viz-tooltip.PNG
[data-screenshot-before]: images/raw-dataset-screenshot.png
[cleaned-route-screenshot]: images/cleaned-route-screenshot.png
[data-cleaning-notebook]: https://github.com/paulabondoc/airline-ratings-data-project/blob/main/Script1%20-%20Data_cleaning.ipynb

[Tableau-viz]: https://public.tableau.com/app/profile/paula.bondoc/viz/Whatisthebestairlineforyourtrip/AirlineReviewsDashboard
[raw-data]: https://www.kaggle.com/datasets/joelljungstrom/128k-airline-reviews/data
