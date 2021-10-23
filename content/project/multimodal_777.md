+++
title = "Improving Action Segmentation on Large Egocentric Cooking Dataset"
summaryTitle = "Improving Action Segmentation on Large Egocentric Cooking Dataset"
postSummary = "For 11-777 Multimodal Machine Learning, our team tackled the problem of action segmentation on the EPIC-KITCHENS dataset."
tags = [
    "senior_year",
    "term_project",
]
categories = [
    "senior_year",
]
date = "2021-05-04"
+++

## Abstract
The task of action segmentation involves identifying not only the start and end time of different actions in an untrimmed video but also the action types. Previous approaches take in only visual inputs,  whereas we attempt to  solve the task using additional text input. We test our methods on the EPIC-KITCHENS dataset, whose narration annotations allow us to learn a visual-textual joint-embedding. We build upon the existing MS-TCN model which produces the start and end time of segments in a video, and we uses the visual features of the predicted segment to retrieve the closest narration in terms of their distance in the joint space. Although the video-text retrieval componentdoes not improve baseline performance, we analyze its strength in terms of action recognition and the causes of potential failure cases. 