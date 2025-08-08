# Portfolio – Analyse et Modélisation de Graphes

##  Objectif
Ce portfolio regroupe deux analyses complémentaires de graphes dans le cadre d’exercices académiques :  
1. **Analyse d’un graphe réel** de citations en physique des hautes énergies  
2. **Modélisation** de ce graphe à l’aide de l’algorithme **DPA** (*Directed Preferential Attachment*)  

L’objectif est de comparer la **distribution des degrés d’entrée** d’un graphe réel à celle d’un graphe généré artificiellement, et de constater la présence d’une **loi de puissance**.

---

##  Contenu du portfolio
### 1. Graphe de citations réel
- **Source** : fichier `alg_phys-cite.txt` (27 770 nœuds, 352 768 arêtes)  
- **Notebook** : `degree_distribution_loglog.ipynb`  
- **Résultat** : distribution normalisée des degrés (log–log)  
![Distribution log–log graphe réel](degreededistributionlog_graphe.png)

---

### 2. Graphe DPA simulé
- **Paramètres utilisés** :  
  - `n = 27 770` nœuds  
  - `m = 13` arêtes sortantes par nouveau nœud  
- **Notebook** : `dpa_indegree_distribution_loglog.ipynb`  
- **Résultat** : distribution normalisée des degrés d’entrée (log–log)  
![Distribution log–log graphe DPA](degrédedistributionsdesentrées_graphe.png)

---

##  Méthodologie

### Partie 1 – Graphe de citations réel
1. Chargement du graphe depuis un fichier texte (dictionnaire d’adjacence)  
2. Calcul de la **distribution des degrés**  
3. Normalisation (somme des fréquences = 1)  
4. Tracé du **log–log** (exclusion des degrés 0)

### Partie 2 – Graphe DPA
1. Initialisation par un graphe complet à `m` nœuds  
2. Utilisation de la classe **DPATrial** pour ajouter les nouveaux nœuds selon la loi de préférence attachée  
3. Calcul de la distribution des **degrés d’entrée**  
4. Normalisation et tracé log–log  

---

##  Exécution
Les notebooks et scripts fournis sont directement exécutables sans modification préalable du code.

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/CDestine/Rice_university_project.git
