# LamenessDetection

### NEED OF LAMENESS DETECTION 
The prevalence of lameness has been reported differently in different regions and states. Ger reported that on an average Irish farm, 20 in every 100 cows are affected by lameness in a given year. Timely detection of lameness is a big problem in the dairy industry which farmers are not yet able to adequately solve. It is one of the factors for reduced performance on many dairy farms, at least through reduced reproductive efficiency, milk production and increased culling . Lameness in sheep is the biggest cause of concern regarding poor health and welfare among sheep producing countries. 

### PROPOSED MODEL
So now we have the challenge to detect lameness considering three important points-
>- If we could detect lameness in sheep using both accelerometer and gyroscope signals, 
>- Which machine learning algorithms perform best at classifying lameness and what are the most important features for lameness classification
>- If we can classify lameness in sheep across a range of daily activities (walking, standing and lying).


### ALGORITHM USED
So firstly, classified the sheep firstly on the basis of walking, standing and lying. Also to collect data statistics the given data is classified into lame and non-alme sheep ids. Then applied a feature selection process to order and rank features according to their importance. Feature selection in this study was carried out using a filter-based approach using ReliefF.
Once a sheep's activity was identified, a second classifier was applied in order to classify if a sheep is lame or not.
The classification algorithms which I have used to detect lameness are Random Forest (RF) and K-Nearest Neighbour (KNN). Both algorithms are implemented using the ‘scikit-learn’ package using the set of 32 previously described feature characteristics as input variables and the corresponding ground truth lameness and behaviour for each of the window samples as labels.

#### RF(Random Forest) Algorithm 
In the RF algorithm, the number of trees was set to 250, with a minimum sample count set for leaf nodes equal to 1, and with the number of features to consider when looking for the best split equal to the square root of the n features.
#### KNN(K-Nearest Neighbour) Algorithm 
For the KNN algorithm, K was set to 5, the distance metric was Euclidean and no normalization was adopted during the training as it did not significantly improve overall performance.


