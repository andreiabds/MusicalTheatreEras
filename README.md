# Musical Theatre Eras: An Analysis

## Abstract: 
Musical Theatre can be traced back to ancient Greek theatre, where plays would have song and dance. However, Musical Theatre in the format we consume nowadays is dated from the late 1800's, and since then Musicals evolved and had many different eras. 
However, there is no consensus about how many eras exist and when each era starts. The only consensus is that there is a period called "Golden Age" that happened through the 1940's to the 1960's. 

This analysis proposes to use data (audio features from musical songs) to bring more clarity to eras of musicals. 

We first train a K-means clustering algorithm and use the Elbow Method to identify the optimal number of cluster (Musical Theatre Eras). We found unclear results, thus validating the discussion; it is indeed a hard task to clearly identify Musical Theatre eras.

Then we trained Random Forest Classifier to (1) understand if we can classify musical songs into three eras (Pre-Golden Age, Golden Age, Post-Golden Age) with good accuracy and (2) identify which features were more important for this classification. We were able to train a model with 70% accuracy (better than majority class baseline 55.9%).

Finally, we tested a few hypothesis about the three periods we identified in our classifier. Using the MannWhitney U test, we discovered that Modern/Contemporary Musicals (Post-Golden Age) have songs with more loudness, more speechiness, and longer duration; while Early Age Musicals (Pre-Golden Age) have songs with slower tempo. 

You can see the analysis [here](https://github.com/andreiabds/MusicalTheatreEras/blob/main/Musical%20Theater%20Era%20Analysis.ipynb).


## The Dataset
The dataset is available [here](https://github.com/andreiabds/orpheus/blob/master/data/COMPLETE_DATA.csv). 
It was created by combining data from [Spotify API](https://developer.spotify.com/documentation/web-api/reference/object-model/#audio-features-object), [Wikipedia](https://en.wikipedia.org/wiki/List_of_musicals:_A_to_L), and [Stlyrics.com](https://www.stlyrics.com/). 

|FIELD|VALUE TYPE|VALUE DESCRIPTION|
|-----|----------|-----------------|
|sp_track_id|string|unique Id for the song track from Spotify API|
|wikipedia_title|string|Musical Theatre title found on Wikipedia|
|acousticness|float|A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|danceability|float|Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. |
|duration_ms|int|The duration of the track in milliseconds.|
|energy|float|Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.|
|instrumentalness|float|Predicts whether a track contains no vocals. |
|key|int|The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.|
|liveness|float|Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.|
|loudness|float|The overall loudness of a track in decibels (dB). Values typical range between -60 and 0 db.|
|mode|int|Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. |
|speechiness|float|Speechiness detects the presence of spoken words in a track|
|tempo|float|in beats per minute (BPM).  In musical terminology, tempo is the speed or pace of a given piece.|
|time_signature|int|An estimated overall time signature of a track.|
|valence|float|A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. |
|year|int|year the musical was premiered|
|lyrics|string|lyrics for the song|
|composer_label|int|id identifying the composer(s) to composer mapping.|
|lyricist_label|int|id identifying the lyricist(s) to lyricist mapping.|

## License
You can find the license file [here](https://github.com/andreiabds/MusicalTheatreEras/blob/main/LICENSE).
