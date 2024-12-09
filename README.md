# EcommerceCustomerSegmentation

Projet de segmentation des clients d'un site e-commerce utilisant des méthodes d'apprentissage non supervisé (K-means, Clustering hiérarchique). Analyse des comportements d'achat et des données démographiques pour identifier des segments de clients et proposer des recommandations pour les campagnes marketing et la maintenance des segments.

## Description
Ce projet a pour objectif de :  
1. **Segmenter les clients** d'un site e-commerce à l'aide de méthodes non supervisées (K-means, clustering hiérarchique, DBSCAN).  
2. **Analyser les segments** pour fournir des recommandations marketing basées sur les comportements d'achat.  
3. **Tester la stabilité des segments dans le temps** pour proposer un contrat de maintenance.  

## Contenu du projet
1. **Description et nettoyage des données** :  
   - Données issues de [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).  
   - Nettoyage des valeurs manquantes et aberrantes, regroupement des catégories de produits.  

2. **Analyse exploratoire** :  
   - Étude des comportements d'achat, satisfaction client, et corrélations entre variables.  
   - Variables principales : délais de livraison, satisfaction, localisation, RFM (récence, fréquence, montant).  

3. **Feature Engineering** :  
   - Création de nouvelles variables (retard de livraison, pourcentage par type d'énergie, etc.).  
   - Transformation logarithmique pour les variables non normalisées.  

4. **Modélisation** :  
   - Méthodes testées :  
     - K-means (modèle final).  
     - Clustering hiérarchique (agglomératif).  
     - DBSCAN.  
   - Évaluation des clusters à l’aide de métriques (Silhouette Score, Davies-Bouldin, Calinski-Harabasz).  

5. **Stabilité des clusters** :  
   - Analyse avec l’indice de Rand Ajusté (ARI).  
   - Proposition de mise à jour du modèle tous les 5-6 mois pour garantir la pertinence.  

## Résultats
- **Clustering retenu :** K-means avec 6 variables numériques, 5 clusters bien séparés.  
- **Exemple de segments identifiés :**  
  - Clients réguliers avec montant élevé (top clients).  
  - Clients mécontents ayant commandé peu d’articles.  
  - Clients prometteurs avec des comportements d’achat modérés.  

## Technologies utilisées
- **Python** : pandas, NumPy, scikit-learn, matplotlib, seaborn.  
- **Algorithmes de clustering** : K-means, DBSCAN, clustering hiérarchique.  

## Prochaines étapes
- Approfondir les recommandations pour chaque segment.  
- Optimiser les algorithmes pour des jeux de données plus larges.  
