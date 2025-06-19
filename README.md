# OrangeClientAnalytics

## Nom / Prénom  
Songho Armel Joel

---

## Librairies utilisées  
- pandas  
- numpy  
- scikit-learn (StandardScaler, KMeans, PCA, TSNE)  
- matplotlib  
- seaborn  

---

## Résumé des observations

Le dataset client comprend des variables clés telles que l’âge, la durée des appels, le volume de données consommées, le nombre de SMS envoyés, le montant de la facture, ainsi que la région et le type de forfait.

Une première analyse exploratoire révèle :  
- Une distribution relativement normale des volumes de données et du temps d’appels, avec quelques valeurs extrêmes.  
- Des montants de factures variant selon les types de forfaits, avec des différences significatives visibles sur les boxplots.  
- Une concentration variable du nombre de clients selon les régions, certaines régions regroupant une majorité de clients.

La segmentation client par clustering KMeans (avec standardisation des variables numériques) a permis d’identifier deux groupes distincts, visualisés par une projection PCA en deux dimensions.

Un profil de clients à « fort potentiel » a été défini sur la base de critères métiers :  
- Consommation de données élevée (au-dessus du 75e percentile)  
- Montant de facture relativement bas (en dessous de la médiane)  
- Forfait de type prépayé

Ce profil, illustré par un scatter plot des données vs montants factures, identifie un segment stratégique pour des actions marketing ciblées.

---

## Recommandations business

- **Cibler le segment "Fort Potentiel" avec des offres adaptées** permettant de maximiser leur consommation tout en augmentant la valeur client (ex : promotions sur data illimitée, offres spécifiques prépayées).  
- **Optimiser les campagnes régionales** en fonction des zones géographiques où la concentration de clients est la plus élevée.  
- **Personnaliser les offres en fonction des clusters** identifiés, notamment en adaptant les services aux comportements de consommation distincts.

---

## Ce qui aurait pu être ajouté avec plus de temps

- Tester et comparer d’autres algorithmes de clustering (DBSCAN, Agglomératif) pour mieux capturer la complexité des profils clients.  
- Intégrer des variables supplémentaires, comme l’historique des recharges ou des appels à l’international, pour enrichir l’analyse.  
- Mener une analyse plus fine des clusters via des méthodes d’interprétabilité ou des visualisations avancées (t-SNE, UMAP).  
- Implémenter une validation croisée ou silhouette score pour optimiser le nombre de clusters.

