## UNSUPERVISED LEARNING ON CITY OF SCOTTSDALE CITATIONS
### PROJECT OVERVIEW
#### Three clustering methods will be used to look for patterns in when different demographics receive certain types of citations.  Specifically, clusters will be formed using CITATION TYPE, LOCATION, AGE, TIME OF DAY, DAY OF WEEK, and MONTH OF YEAR.


#### Applications for this Analysis:

1. By undersanding when and where certain demographics are more likely to receive citations the city could be more proactive in preventing the citations.  Additionally, this could allow the city to be more effective in assigning its police force.

1. Selling services to people who receive citations:  
    - Lawyers or professionals providing services to people who receive and want to contest certain types of citations could use clustering information to inform where to market their services.
    - Ride hailing services such as Lyft and Uber would benefit by being able to identify areas and specific times when people might be most likely to drive drunk.  Using targeted advertising these companies can more effictively market their services and keep drunk drivers off the roads.
    
1.  Providing information for citizens to be more careful within certain areas of the city.  Similar to how the navigation app Waze crowd sources information to prevent people from receiving a ticket, identifying specific clusters and allerting people to them may prevent them from receiving citations.
 
4. Historical citations represent a picture of past policing practices.  Understanding citation clusters in the past can provide a context for distributing policing forces in the future.  Perhaps clusters are forming in some places simply because police officers perceive that policing that area to be the best use of their time.  When in fact there are other areas that are being overlooked.   

### PROJECT RESULTS
With an end goal of providing specific, actionable recommentations related to which areas of town have the highest concentrations of specific citations being received by people within different demographics DBSCAN was was the clear winner.

The clusters it revealed were not entirely surprising to me.  If I were to focus on cluster groupings for clusters smaller than the top 50, its possible I find find others clusters that have more specific characteristics.

However, within the top 50 DBSCAN clusters, all the clusters were formed around a single citation and location.  Clearly the categories were playing a disproportionate role in the clustering.  

One admirable quality in GMM and Hierarcical clustering is their ability to include more than one citation type and location within each cluster.  With enough tuning it may be possible I could get one of these models to identify clusters as tight as DBSCAN.

## DBSCAN Clustering
*****

Parameter tuning based on cluster fit.

![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_silhouette_cluster.PNG)

Based on the parameters I used to tune DBSCAN, the below pie chart was the resulting cluster distribution.

![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_cluster_distributions.PNG)

Demographic characteristics associated with each cluster.  All the clusters are made up of one categorical variable each (citation type, and location).  
1. Both clusters 55 and 79 show similar characteristics - lower age and hour of the day with later day of the week.  
1. Cluster 101 and 98 represent the oldest people receiving citations, these are happening at a relatively early day of the day.  
1. Cluster 78 represents the youngest people receiving ciations.
1. Cluster 58 represents the latest citations happening in the day, with no pattern in the age or time of day that these citations are issued.

![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_cluster_characteristics.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_1.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_2.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_3.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_5.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_6.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_7.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_8.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/dbscan_clusters_9.PNG)

## GMM Clustering
******
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_silhouette_cluster.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_cluster_distribution.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_cluster_characteristics.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_clusters_1.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_clusters_2.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/gmm_clusters_3.PNG)

## Hierarcical Clustering
******
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/hierarchical_cluster_distributions.PN)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/hierarchical_cluster_characteristics.PNG)
![](https://github.com/mrkjhsn/Unsupervised_Learning_Scottsdale_Citations/blob/master/visualizations/hierarchical_clusters_1.PNG)





