# Group_recommendation_system with GcPp clustering

A Jupyter notebook for a project centered around 'Group Recommendation Systems (GRS)' utilizing the 'GcPp' clustering approach.
"A Graph Neural Approach for Group Recommendation System based on Pairwise Preferences (Information Fusion 2024)"

<div style="display: flex;">
    <img src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Images/Similarity_prediction.png" alt="Description of the First Image" style="width: 46%;">
    <img src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Images/Clustering_GcPp.png" alt="Description of the Second Image" style="width: 48%;">
</div>

### Abstract

Pairwise preference information, which involves users expressing their preferences by comparing items, plays a crucial role in decision-making and has recently found application in recommendation systems. In this project, we introduce GcPp, a clustering algorithm that leverages pairwise preference data to generate recommendations for user groups. Initially, we construct individual graphs for each user based on their pairwise preferences and utilize a graph convolutional network to predict similarities between all pairs of graphs. These predicted similarity scores form the foundation of our research. We then construct a new graph where users are nodes and the edges are weighted according to the predicted similarities. Finally, we perform clustering on the graph's nodes (users). By evaluating various metrics, we found that employing a similarity metric based on a convolutional neural network (SimGNN) with our proposed ground truth called Top-K yielded the highest accuracy. The proposed approach is specifically designed for group recommendation systems and holds significant potential for group decision-making problems. 

### Requirements
The codebase is implemented in Python 3.10.9. package versions used for development are just below.
```
networkx          2.8.4
tqdm              4.64.1
numpy             1.23.4
pandas            1.5.3
texttable         1.6.4
scipy             1.10.0
torch             1.12.1
torch-scatter     2.0.9
torch-sparse      0.6.15
torch-cluster     1.6.0
torch-geometric   2.1.0
torchvision       1.13.1
scikit-learn      1.1.2
```

### Dataset
The [dataset comprises car preferences](http://users.cecs.anu.edu.au/~u4940058/CarPreferences.html) that were provided by Abbasnejad et al. in 2013. The dataset was gathered from 60 users residing in the United States, who participated in the data collection process through [Amazon's Mechanical Turk](http://mturk.com). The dataset focuses on ten distinct cars, treated as individual items for comparison purposes. Each user in the dataset provided responses for all 45 possible pairs of items, resulting in a total of 90 observations for each expert. In addition to the pairwise preference scores, the dataset also includes two additional files containing users' attributes (education, age, gender, and region) and car attributes (body type, transmission, engine capacity, and fuel consumed). However, in our project, neither the users' attributes nor the cars' attributes were used during the training of the model.

### Results (Evaluation)
After implementing the clustering method, you can view the subsequent plot, illustrating the training and testing loss.
<p align="center">
<img style="width: 80%;" src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Images/GcPp_evaluation.png">
</p>
Additionally, upon executing the code related to the 'group recommendation system,' a plot similar to the following will be displayed:
<p align="center">
<img style="width: 40%;" src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Images/GRS_evaluation.png">
</p>

----------------------------------------------------------------------

**License**

[MIT License](https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/LICENSE)







