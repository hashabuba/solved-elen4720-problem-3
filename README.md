Download Link: https://assignmentchef.com/product/solved-elen4720-problem-3
<br>
<h1>Problem 1 (K-means)</h1>

Implement the K-means algorithm discussed in class. Generate 500 observations from a mixture of three

Gaussians on R<sup>2 </sup>with mixing weights <em>π </em>= [0<em>.</em>2<em>,</em>0<em>.</em>5<em>,</em>0<em>.</em>3] and means <em>µ </em>and covariances Σ,

<em> .</em>

<ol>

 <li>For <em>K </em>= 2<em>,</em>3<em>,</em>4<em>,</em>5, plot the value of the K-means objective function per iteration for 20 iterations (the algorithm may converge before that).</li>

 <li>For <em>K </em>= 3<em>,</em>5, plot the 500 data points and indicate the cluster of each for the final iteration by marking it with a color or a symbol.</li>

</ol>

<h1>Problem 2 (Bayes classifier revisited)</h1>

In this problem, you will implement the EM algorithm for the Gaussian mixture model, with the purpose of using it in a Bayes classifier. The data is a processed version of the spam email data you looked at in Homework 2. Now, each labeled pair (<em>x,y</em>) has <em>x </em>∈R<sup>10</sup>. We discussed how the Bayes classifier learns class-conditional densities, and unsupervised learning algorithms can be useful here. In this problem, the class conditional density will be the Gaussian mixture model (GMM). In these experiments, please initialize all covariance matrices to the empirical covariance of the data being modeled. Randomly initialize the means by sampling from a single multivariate Gaussian where the parameters are the mean and covariance of the data being modeled. Initialize the mixing weights to be uniform.

<ol start="30">

 <li>Implement the EM algorithm for the GMM described in class. Using the training data provided,for each class separately, plot the log marginal objective function for a 3-Gaussian mixture model over 10 different runs and for iterations 5 to 30. There should be two plots, each with 10 curves.</li>

 <li>Using the best run for each class after 30 iterations, predict the testing data using a Bayes classifierand show the result in a 2 × 2 confusion matrix, along with the accuracy percentage. Repeat this process for a 1-, 2-, 3- and 4-Gaussian mixture model. <em>Show all results nearby each other, and don’t repeat Part (a) for these other cases. </em>Note that a 1-Gaussian GMM doesn’t require an algorithm, although your implementation will likely still work in this case.</li>

</ol>

<h1>Problem 3 (Matrix factorization)</h1>

In this problem, you will implement the MAP inference algorithm for the matrix completion problem discussed in class. As a reminder, for users <em>u </em>∈R<em><sup>d </sup></em>and movies <em>v </em>∈R<em><sup>d</sup></em>, we have <em>u<sub>i </sub></em>∼ <em>N</em>(0<em>,λ</em><sup>−1</sup><em>I</em>)<em>, i </em>= 1<em>,…,N</em><sub>1</sub><em>, v<sub>j </sub></em>∼ <em>N</em>(0<em>,λ</em><sup>−1</sup><em>I</em>)<em>, j </em>= 1<em>,…,N</em><sub>2</sub><em>.</em>

We are given an <em>N</em><sub>1</sub>× <em>N</em><sub>2 </sub>matrix <em>M </em>with missing values. Given the set Ω = {(<em>i,j</em>) : <em>M<sub>ij </sub></em>is measured}, for each (<em>i,j</em>) ∈ Ω we model <em>M<sub>ij </sub></em>∼ <em>N</em>(<em>u<sup>T</sup><sub>i </sub>v<sub>j</sub>,σ</em><sup>2</sup>).

You should run your code on the user-movie ratings dataset provided on Courseworks and the course website. For your algorithm, set <em>σ</em><sup>2 </sup>= 0<em>.</em>25, <em>d </em>= 10 and <em>λ </em>= 1. Train the model on the larger training set for 100 iterations. For each user-movie pair in the test set, predict the rating using the relevant dot product. Note that the mean rating has been subtracted from the data and you do not need to round your prediction. Since the equations are in the slides, there’s no need to re-derive it.

<ol>

 <li>Run your code 10 times. For each run, initialize your <em>u<sub>i </sub></em>and <em>v<sub>j </sub></em>vectors as <em>N</em>(0<em>,I</em>) random vectors. On a <em>single </em>plot, show the the log joint likelihood for iterations 2 to 100 for each run. In a table, show in each row the final value of the training objective function next to the RMSE on the testing set. Sort these rows according to decreasing value of the objective function.</li>

</ol>

For the run with the highest objective value, pick the movies “Star Wars” “My Fair Lady” and“Goodfellas” and for each movie find the 10 closest movies according to Euclidean distance using their respective locations <em>v<sub>j</sub></em>. List the query movie, the ten nearest movies and their distances. A mapping from index to movie is provided with the data