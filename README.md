# Group_recommendation_system with GcPp clustering

A Jupyter notebook for a project centered around 'Group Recommendation Systems (GRS)' utilizing the 'GcPp' clustering approach.
"A Graph Neural Approach for Group Recommendation System based on Pairwise Preferences (Information Fusion 2024)"

<div style="display: flex;">
    <img src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Similarity_prediction.png" alt="Description of the First Image" style="width: 40%;">
    <img src="https://github.com/RozaAbolghasemi/GRS_GcPp/blob/main/Clustering_GcPp.png" alt="Description of the Second Image" style="width: 42%;">
</div>

##Abstract
Pairwise preference information, which involves users expressing their preferences by comparing items, plays a crucial role in decision-making and has recently found application in recommendation systems. In this study, we introduce GcPp, a clustering algorithm that leverages pairwise preference data to generate recommendations for user groups. Initially, we construct individual graphs for each user based on their pairwise preferences and utilize a graph convolutional network to predict similarities between all pairs of graphs. These predicted similarity scores form the foundation of our research. We then construct a new graph where users are nodes and the edges are weighted according to the predicted similarities. Finally, we perform clustering on the graph's nodes (users). By evaluating various metrics, we found that employing a similarity metric based on a convolutional neural network (SimGNN) with our proposed ground truth called Top-K yielded the highest accuracy. The proposed approach is specifically designed for group recommendation systems and holds significant potential for group decision-making problems. 


