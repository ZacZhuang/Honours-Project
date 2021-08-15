# Honours-Project
# Project： clustering distance computing

## Prerequisite
Anaconda 3  
tinker  
numpy  1.19.5  
matplotlib  2.2.2  
PIL  5.1.0     *pip install pillow*


## Usage
Step1： enter current directory and open command line  
Step2： python3 dist_gui.py


## Algorithm


### **point distance representation**
A n x m matrix is used for point distance representation, where n represents the ith point in cluster 1, and m represents the jth point in cluster 2.  

More details please refer to function *get_dists(x_list, y_list)* and *def detect_two_circle_points(x_list1, y_list1, x_list2, y_list2)*

### **Compute1: point distances computing among inner clusters**
**pseudo code**   
**step1** : input clustering number and init figure by generating clustering points  
**step2** : set *i=0* , choose ith clustering  
**step3** : compute point distances among this inner cluster, and store all distance in matrix *dists*  
**step4** : set *i = i+1* , and repeat step2, until iterate all clusters  
**step5** : compare matrix *dists* with specified threshold and return index representing point position  
**step6** : highlight points with red cicle if exceeding threshold

### **Compute2: cluster center distances computing among each two clusters** 
**pseudo code**   
**step1** : input clustering number and init figure by generating clustering points  
**step2** : set *i=0* , choose ith cluster center  
**step3** : compute cluster center distances between ith cluster with the rest of clusters, and update distance matrix *dists*  
**step4** : set *i = i+1* , and repeat step3, until iterate all clusters  
**step5** : compare matrix *dists* with specified threshold and return index representing cluster center position  
**step6** : highlight cluster circle with purple line if exceeding threshold

### **Compute3: point distances computing among each two clusters**
**pseudo code**   
**step1** : input clustering number and init figure by generating clustering points  
**step2** : set *i=0* , choose all points in ith cluster  
**step3** : compute all point distances in ith cluster with regard to the points of each rest of clusters, and update distance matrix *dists*  
**step4** : set *i = i+1* , and repeat step3, untill iterate arbitrary two clusters  
**step5** : compare matrix *dists* with specified threshold and return index representing point positions  
**step6** : highlight points with diamond style if exceeding threshold
