# FRIEND_RECCO

From the input data we first make a directed graph.Then based on that directed graph we want to predict whether there is a missing link between two id's or not.We first calculate some features from the directed graph. <br />
Features are given below-<br />
</pre> &nbsp; Jaccard Distance, Cosine Distance, Page Ranking, Shortest Path, ADAR index ,Katz Score,whether follow back and some SVD features of adjoint matrix and some weight features.<br />
Now we have two option to check -<br />
   </pre> &nbsp;  &nbsp; 1.Whether Two Person can be friend or not<br />
We used decision based model like random forest,xgboost and probabilistic model like logistic regression,svm to predict the classes('Yes' or 'No').<br />
  </pre> &nbsp; &nbsp; 2.Suggest top 10 friend for a particular person based on probability score<br />
We first find features by keeping source node equal to that person and varying destination node for all users.Then we used logistic regression and svm to predict probability score from these features.Best on the maximum probabilities we suggest top 10.  <br />   
