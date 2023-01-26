# Data-Wrangling-pj1
### Data Wrangling Report

**Introduction:**

**This report details the data wrangling efforts undertaken on the Twitter_archive_enhanced, tweet-json.txt, and image_predictions datasets. The goal of these efforts was to address a number of issues related to data quality and tidiness, in order to make the data more usable for analysis**


* **A. Quality Issues:**


* Invalid names in the "name" column of the Twitter_archive_enhanced dataset: During the initial assessment of the data, it was discovered that some of the entries in the "name" column contained invalid names such as "a" and "an". These entries were cleaned by replacing them with "None" to indicate that no name was provided.

* Removing links from the "text" column of the Twitter_archive_enhanced dataset: The "text" column of the Twitter_archive_enhanced dataset contains tweets, some of which include links. These links were removed from the text column to make the data cleaner.

* Invalid datatype of "timestamp" column to timestamp: The "timestamp" column was in string format, but it need to be converted to timestamp data type in order to perform any time series analysis on it.

* Rename "ID" to "tweet_id" in the tweet-json.txt dataset: The "ID" column in the tweet-json.txt dataset was renamed to "tweet_id" to be consistent with the naming conventions used in the other datasets.

* Invalid datatype of "tweet_id" to object (string): The "tweet_id" columns from all datasets was in int format, but it need to be converted to object (string) data type for consistency across the datasets and for the merging process.

* Invalid data in the "retweet_count" and "favorite_count" columns of the tweet-json.txt dataset: The "retweet_count" and "favorite_count" columns of the tweet-json.txt dataset contained some invalid data, such as negative values and non-numeric values. These were cleaned by replacing them with "None" to indicate that no count was provided.

* "p1,p2,p3" column contains lowercase and uppercase names in the image_predictions dataset: The "p1" column in the image_predictions dataset contains some entries that have different capitalization. These entries were cleaned by converting them to lowercase in order to be consistent.

* Invalid data in "rating_denominator" and "rating_numerator" columns of the Twitter_archive_enhanced dataset: The "rating_denominator" and "rating_numerator" columns of the Twitter_archive_enhanced dataset contained some invalid data, such as zero and non-numeric values. These were cleaned by replacing them with "None" to indicate that no rating was provided.


* **B. Tidiness Issues:**


* Extract text from the 'doggo', 'floofer', 'pupper', 'puppo' columns to create new column called "dog type" of the Twitter_archive_enhanced dataset: The 'doggo', 'floofer', 'pupper', 'puppo' columns in the Twitter_archive_enhanced dataset were redundant, so new column called "dog_type" was created to extract the text value from these columns to make the data more tidy.

* Merging the 3 datasets by "tweet_id": All three datasets were merged on the "tweet_id" column to create a single, unified
