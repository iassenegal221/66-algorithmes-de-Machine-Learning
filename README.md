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
- L'algorithme PCA projette des observations sur les composants principaux de la matrice de caractéristiques qui conservent le plus de variance. PCA peut également être utilisée dans le scénario, où nous avons besoin de conserver des fonctionnalités qui partagent une variance maximale. PCA est implémenté dans scikit-learn en utilisant la méthode PCA :

      class sklearn.decomposition.PCA(n_components=None, *, copy=True, whiten=False, svd_solver='auto', tol=0.0, iterated_power='auto', random_state=None)

- Le parametre n_components a deux opérations, selon l'argument fourni. Si l'argument est supérieur à 1, n_components renverra autant de fonctionnalités. Si l'argument de n_components est compris entre 0 et 1, PCA renvoie le nombre minimum d'entités qui conservent autant de variance. Il est courant d'utiliser des valeurs de 0,95 et 0,99, ce qui signifie que 95 % et 99 % de la variance des caractéristiques d'origine ont été conservées.
- whiten =True transforme les valeurs de chaque composante principale afin qu'elles aient une moyenne nulle et une variance unitaire. Le blanchiment supprimera certaines informations du signal transformé mais peut parfois améliorer la précision prédictive des estimateurs en aval.
- svd_solver=" randomized", qui implémente un algorithme stochastique pour trouver les premières composantes principales en souvent beaucoup moins de temps.

- Référence:
  - [**Machine Learning From Scratch**](https://dafriedman97.github.io/mlbook/content/introduction.html)
  - [**Scikit-learn Implementation**](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html) 

**💡 Algorithme 3 : RBF Kernel PCA**: 

- Standard PCA uses linear projection to reduce the features. If the data is linearly separable then PCA works well. However, if your data is not linearly separable, then linear transformation will not work as well as expected. In this scenario, Kernel PCA will be useful. Kernel PCA uses a kernel function to project a dataset into a higher dimensional feature space, where it is linearly separable, this is called the Kernel trick. The most commonly used Kernel PCA is Gaussian radial basis function kernel RBF.
- RBF Kernel PCA is carried out in the following steps

      1. Computation of Kernel Matrix: 
            We need to compute kernel matrix for every point i.e., if there are 50 samples in a dataset, this step will result in a 50x50 kernel matrix.
      
      2. Eigen-decomposition of Kernel Matrix:
            To make the kernel matrix centered, we are applying this step and to obtain the eigenvectors of the centered kernel matrix that correspond to the largest eigenvalues.
 
- Reference:
  - [**Machine Learning with Python Cookbook**](https://www.amazon.in/Machine-Learning-Python-Cookbook-Preprocessing/dp/9352137302/ref=sr_1_1?crid=3SWKWJG6II2GK&keywords=machine+learning+with+python+cookbook&qid=1636010115&sprefix=Machine+Learning+with+Python+%2Caps%2C273&sr=8-1)


**💡 Linear Discriminant Analysis**: 
-  LDA is a classification that is also a popular technique for dimensionality reduction. In PCA we were only interested in the component axes that maximize the variance in the data, while in LDA we have the additional goal of maximizing the differences between classes. In scikit-learn, It is implemented using LinearDiscriminantAnalysis, which includes a parameter, n_components, indicating the number of features we want to be returned, which can be determined using explained_variance. PCA is unsupervised whereas LDA is supervised.
- LDA is carried out in the following steps

      1. Calculate between-class scatter(S_B)
      2. Calculate in-class scatter(S_W)
      3. Calculate Eigenvalues of (Inverse of in-class scatter)*(between-class scatter)
      4. Sort the Eigenvectors according to their Eigenvalues in decreasing order
      5. Choose first k Eigenvectors and that will be new k dimensions(Linear Discriminants)
      6. Transform the original n-dimensional data points into k dimensions.
    
- Reference:
  - [**Machine Learning with Python Cookbook**](https://www.amazon.in/Machine-Learning-Python-Cookbook-Preprocessing/dp/9352137302/ref=sr_1_1?crid=3SWKWJG6II2GK&keywords=machine+learning+with+python+cookbook&qid=1636010115&sprefix=Machine+Learning+with+Python+%2Caps%2C273&sr=8-1)

