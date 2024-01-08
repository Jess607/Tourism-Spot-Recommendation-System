# Tourism-Spot-Recommendation-System
This is a recommender system that employs the use of hybrid filtering for the recommendation of tourism destination spots to individual and tourist-groups. The recommender system explores the feasibility of traditional predictive modelling techniques(Gradient Boosting Regression) at providing accurate recommendations in our case for the sake of tourism. The aim is to combine the strong predictive abilities of GBR with collaborative filtering(matrix factorization) creating more generally accurate recommendations. 

# Table Of Contents
* [Installation](https://github.com/Jess607/Tourism-Spot-Recommendation-System#installation)
* [About the Project](https://github.com/Jess607/Tourism-Spot-Recommendation-System#about-the-project)
* [Data Gathering](https://github.com/Jess607/Tourism-Spot-Recommendation-System#data-gathering)
* [File Description](https://github.com/Jess607/Tourism-Spot-Recommendation-System#file-description)
* [Licensing And Authors](https://github.com/Jess607/Tourism-Spot-Recommendation-System#licensing-and-authors)

# Installation 
The code requires:
* `python 3 and above`
* `numpy`
* `pandas`
* `sklearn`
* `matplotlib`
* `seaborn`



# About The Project 
Recommender systems have found application in a plethora of sectors from sales and marketing to tourism. The success of business ventures has become closely tied to their ability to recommend the right products and services to prospective customers in search of those products and services. The tourism and leisure sector in recent times has been no stranger to the revenue boom inspired by the impact of recommender systems. The provision of platforms that provide the best recommendations in an easy to navigate manner have proven to be the difference between the most successful and highly rated hotel booking platforms and their less successful counterparts. 

Designing recommender systems that perform opyimally is solely hinged on the quality of the algorithm such recommender system runs on. There are various classifications of recommender systems based on the approach used in their design. They include:
* `Content based filtering recommender systems`
* `Collaborative based filtering recommender systems`
* `Knowledge based filtering recommender systems`
* `Hybrid filtering recommender systems`

Content based filtering systems recommend items to customers based on the similarity between items customers had previously liked and new items with similar features. Very commonly the cosine similarity algorithm is enlisted for content based filtering. Collaborative filtering on the other hand recommends items to individuals based on the ratings of other users of similar items/interests. Algorithms like matrix factorization have been found to be very useful in these systems. In Knowledge based filtering, the system has knowledge of a certain domain and thus makes recommendations based on the needs of a user that utilizes the system. Hybrid filtering recommender systems simply combine the paradigms of two or more of the above for better optimized systems that produce more accurate recommendations. 

In this project, we explore the feasibility of traditional predictive modeling techniques at generating recommendations. Because of its amazing predictive capacity, the gradient boosting technique is applied in conjunction with matrix factorization(a collaborative filtering technique). In order to create a maximally performing hybrid system, it is important to consider the best method of combination for both models. Here, we utilize a weighted hybrid model that assigns weights between 0 and 1 to both models (Gradient Boosting Regression and Matrix Factorization) and then calculates some evaluation metric(in our case, we calculate the root mean square error). We then visualize results using matplotlib. We realized our lowest RMSE (0.5978) when our collaborative filtering model had a weight of 0.75 and gradient boosting 0.25. After which we put our model to work generating recommendations for an hypothetical user of our system.


# Data Gathering 
Data was gathered from kaggle's amazing repository of datasets available for use. Data utilized was synthetically created by authors for the purpose of recommender systems research 

# File Description 
The folder contains:
* `tourism datasets` folder that contains three datasets:
    * `destination_info.csv`: information about the various destination spots that could potentially be recommended to individuals
    * `user_feastures.csv`: Demographic and social features of individuals gathered ( used in cooperation with destination_info to build gradient boosting model for content based filtering)
    * `user_ratings.csv`: Ratings provided by individuals for the various destination spots (used for collaborative filtering)
* `tour.ipynb` a jupyter notebook of the recommender system built.



# Licensing And Authors
This code was created by Jessica Ogwu under the GPL-3.0 license. Please feel free to use the resources as you deem fit.
