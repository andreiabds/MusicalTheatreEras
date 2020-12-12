# Musical Theatre Eras: An Analysis

## Abstract: 
Musical Theatre can be traced back to ancient Greek theatre, where plays would have song and dance. However, Musical Theatre in the format we consume nowadays is dated from the late 1800's, and since then Musicals evolved and had many different eras. 
However, there is no consensus about how many eras exist and when each era starts. The only consensus is that there is a period called "Golden Age" that happened through the 1940's to the 1960's. 

This analysis proposes to use data (audio features from musical songs) to bring more clarity to eras of musicals. 

We first train a K-means clustering algorithm and use the Elbow Method to identify the optimal number of cluster (Musical Theatre Eras). We found unclear results, thus validating the discussion; it is indeed a hard task to clearly identify Musical Theatre eras.

Then we trained Random Forest Classifier to (1) understand if we can classify musical songs into three eras (Pre-Golden Age, Golden Age, Post-Golden Age) with good accuracy and (2) identify which features were more important for this classification. We were able to train a model with 70% accuracy (better than majority class baseline 55.9%).

Finally, we tested a few hypothesis about the three periods we identified in our classifier. Using the MannWhitney U test, we discovered that Modern/Contemporary Musicals (Post-Golden Age) have songs with more loudness, more speechiness, and longer duration; while Early Age Musicals (Pre-Golden Age) have songs with slower tempo. 


## The Dataset
The dataset is available [here] (). 
It was created by combining data from [Spotify API](https://developer.spotify.com/documentation/web-api/reference/object-model/#audio-features-object), [Wikipedia](https://en.wikipedia.org/wiki/List_of_musicals:_A_to_L), and [Stlyrics.com](https://www.stlyrics.com/). 
