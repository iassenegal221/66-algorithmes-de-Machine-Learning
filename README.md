## Institut des Algorithmes du Sénégal

## 66 algorithmes de Machine Learning

[**Linkdin**](https://www.linkedin.com/company/71517780/)
[**Facobook**](https://www.facebook.com/IASSenegal)
[**Web**](https://www.ias.sn/formations/home)

**💡 Algorithme 1 : Analyse des composants principaux (Principal Component Analysis PCA)**: 
- PCA est une technique de réduction de la dimensionnalité qui permet d'identifier les corrélations et les modèles dans l'ensemble de données afin qu'il puisse être transformé en un ensemble de données de dimensions nettement inférieures sans aucune perte d'informations importantes. Il s'agit d'une technique statistique non supervisée utilisée pour examiner les interrelations entre un ensemble de variables. Elle est également connue sous le nom d'analyse factorielle générale où la régression détermine une ligne de meilleur ajustement. Cela fonctionne à condition que, bien que les données dans un espace de dimension supérieure soient mappées sur des données dans un espace de dimension inférieure, la variance ou la propagation des données dans l'espace de dimension inférieure doit être maximale.
- L'algorithme PCA est réalisé selon les étapes suivantes :

      1. Standardization of Data
      
      2. Computing the covariance matrix
      
      3. Calculation of the eigenvectors and eigenvalues
      
      4. Computing the Principal components
      
      5. Reducing the dimensions of the Data.
    
- Reference:
  - [**Machine Learning From Scratch**](https://dafriedman97.github.io/mlbook/content/introduction.html)
  - [**ML from Scratch on Youtube**](https://lnkd.in/gNPM6vW2) 


**💡 Algorithme 2 : Principal Component Analysis using scikit-learn**: 
- PCA projects observations onto the (hopefully fewer) principal components of the feature matrix that retain the most variance. PCA can also be used in the scenario, where we need features to be retained that share maximum variance. PCA is implemented in scikit-learn using the PCA method:

      class sklearn.decomposition.PCA(n_components=None, *, copy=True, whiten=False, svd_solver='auto', tol=0.0, iterated_power='auto', random_state=None)

- n_components has two operations, depending on the argument provided. If the argument is greater than 1,n_components will return that many features. If the argument to n_components is between 0 and 1, PCA returns the minimum amount of features that retain that much variance. It is common to use values of 0.95 and 0.99, meaning 95% and 99% of the variance of the original features has been retained.
- whiten =True transforms the values of each principal component so that they have zero mean and unit variance. Whitening will remove some information from the transformed signal but can sometimes improve the predictive accuracy of the downstream estimators.
- svd_solver=" randomized", which implements a stochastic algorithm to find the first principal components in often significantly less time. 

- Reference:
  - [**Machine Learning From Scratch**](https://dafriedman97.github.io/mlbook/content/introduction.html)
  - [**Scikit-learn Implementation**](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html) 
