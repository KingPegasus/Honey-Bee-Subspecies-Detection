# Honey-Bee-Subspecies-Detection
Work during Kaggle Hackathon ['DS-14 Hackathon'](https://www.kaggle.com/c/ds-14) by [DiceAnalytics.pk](http://diceanalytics.pk/)

<img src="https://dappimg.com/media/image/app/a1b66729fed64f2c9296b6c00510d2aa.png" alt="HB" class="center"/>

## Context
Every third bite of food relies on pollination by bees. At the same time, this past winter honeybee hive losses have exceeded 60% in some states. How can we address this issue? How can we better understand our bees? And most importantly, how can we save them before it's too late?

While many indications of hive strength and health are visible on the inside of the hive, frequent check-ups on the hive are time-consuming and disruptive to the bees' workflow and hive in general. By investigating the bees that leave the hive, we can gain a more complete understanding of the hive itself. For example, an unhealthy hive infected with varroa mites will have bees with deformed wings or mites on their backs. These characteristics can be observed without opening the hive. To protect against robber bees, we could track the ratio of pollen-carrying bees vs those without. A large influx of bees without pollen may be an indication of robber bees. This dataset aims to provide basic visual data to train machine learning models to classify bees in these categories, paving the way for more intelligent hive monitoring or beekeeping in general.

## Data Description
- This dataset contains 4172 train images and 1000 test images.
- Train and Test images are annotated with location, date, health condition and subspecies.
- Test images have missing 'Subspecies" annotation which is actually your Target variable to be predicted.
- The original batch of images was extracted from still time-lapse videos of bees. By averaging the frames to calculate a background image, each frame of the video was subtracted against that background to bring out the bees in the forefront. The bees were then cropped out of the frame so that each image has only one bee. Because each video is accompanied by a form with information about the bees and hive, the labeling process is semi-automated. Each video results in differing image crop quality levels.
- -1 in SubSpecies column means the information is coming soon, so it is unknown.

## Evaluation
The evaluation metric for this competition is Mean F1-Score. The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn). The F1 score is given by:
<img src="https://miro.medium.com/max/752/1*UJxVqLnbSj42eRhasKeLOA.png" alt="F1 Score Formula" title="F1 Score Formula" />

The F1 metric weights recall and precision equally, and a good retrieval algorithm will maximize both precision and recall simultaneously. Thus, moderately good performance on both will be favored over extremely good performance on one and poor performance on the other.

## Help Material
Some more links for help:
- [Image Processing Using Python OpenCV](https://likegeeks.com/python-image-processing/)
- [Resize Image in OpenCV](https://medium.com/@manivannan_data/resize-image-using-opencv-python-d2cdbbc480f0)
- [Python os library tutorial](https://www.tutorialsteacher.com/python/os-module)
