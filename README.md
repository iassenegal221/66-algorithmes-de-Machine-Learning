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
