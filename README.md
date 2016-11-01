# Predicting-Movie-Ratings-using-ALS (Spark-Mllib)
# CS 110- Lab2 -EdX

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"> <img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png"/> </a> <br/> This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"> Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License. </a>


#![Spark Logo](http://spark-mooc.github.io/web-assets/images/ta_Spark-logo-small.png) + ![Python Logo](http://spark-mooc.github.io/web-assets/images/python-logo-master-v3-TM-flattened_small.png)

<img src="http://spark-mooc.github.io/web-assets/images/cs110x/movie-camera.png" style="float:right; height: 200px; margin: 10px; border: 1px solid #ddd; border-radius: 15px 15px 15px 15px; padding: 10px"/>

# Predicting Movie Ratings

One of the most common uses of big data is to predict what users want.  This allows Google to show you relevant ads, Amazon to recommend relevant products, and Netflix to recommend movies that you might like.  This lab will demonstrate how we can use Apache Spark to recommend movies to a user.  We will start with some basic techniques, and then use the [Spark ML][sparkml] library's Alternating Least Squares method to make more sophisticated predictions.

For this lab, we will use a subset dataset of 20 million ratings. This dataset is pre-mounted on Databricks and is from the [MovieLens stable benchmark rating dataset](http://grouplens.org/datasets/movielens/). However, the same code you write will also work on the full dataset (though running with the full dataset on Community Edition is likely to take quite a long time).

In this lab:
* *Part 0*: Preliminaries
* *Part 1*: Basic Recommendations
* *Part 2*: Collaborative Filtering
* *Part 3*: Predictions for Yourself

As mentioned during the first Learning Spark lab, think carefully before calling `collect()` on any datasets.  When you are using a small dataset, calling `collect()` and then using Python to get a sense for the data locally (in the driver program) will work fine, but this will not work when you are using a large dataset that doesn't fit in memory on one machine.  Solutions that call `collect()` and do local analysis that could have been done with Spark will likely fail in the autograder and not receive full credit.
[sparkml]: https://spark.apache.org/docs/1.6.2/api/python/pyspark.ml.html
