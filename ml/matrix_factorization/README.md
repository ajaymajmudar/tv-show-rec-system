# Matrix Factorization 
This is an implementation of the group recommender algorithms described by Ortega et al. (2016) a the paper titled ["Recommending items to group of users using Matrix Factorization based Collaborative Filtering"](https://www.sciencedirect.com/science/article/pii/S0020025516300196). The base MF algorithms was inspired by [ExplicitMF](https://www.ethanrosenthal.com/2016/01/09/explicit-matrix-factorization-sgd-als/)

Matrix Factorization (MF) Methodology

The MF approach  used is inspired by the virtual user approach from above. This involved aggregating the ratings for all members in a group and creating a rating matrix for input into MF. For the first step of the matrix factorization model, we trained it on the entire dataset to generate a set of embeddings for each anime. Stochastic gradient descent was used to train the model including the bias terms. After, each anime was represented by a 128-dimensional vector. After this, we applied ridge regression to generate embeddings for a virtual user. Using these embeddings, we calculated predicted ratings for the virtual user and filtered the results to get the top recommendations that have not been watched by the group members. Our model implemented and allowed users to modify hyper-parameters such as regularization, aggregation function and method (virtual user vs combining).

