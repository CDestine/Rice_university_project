# Distribution des degrés – Graphe de citations (Physique des hautes énergies)

##  Objectif
Ce projet calcule et affiche la **distribution normalisée des degrés** pour un graphe de citations comprenant **27 770 articles** (352 768 arêtes), selon les consignes du cours *Principles of Computing*.  
Le graphique est présenté en **échelle log/log**.

---

##  Contenu du dépôt
- `degree_distribution_loglog.ipynb` – Notebook Colab avec le code complet  
- `degree_distribution_loglog.png` – Graphique log/log généré  
- `README.md` – Description du projet et instructions

---

##  Données
Le graphe provient de ce fichier texte :  
[alg_phys-cite.txt](http://storage.googleapis.com/codeskulptor-alg/alg_phys-cite.txt)  
Chaque ligne suit ce format :

---

##  Méthodologie
1. Charger le graphe depuis l’URL et le convertir en dictionnaire d’adjacence  
2. Calculer la distribution des degrés (nombre de voisins sortants)  
3. Normaliser cette distribution (somme des fréquences = 1)  
4. Appliquer `log10` aux degrés et fréquences (hors degré 0)  
5. Tracer avec Matplotlib et sauvegarder en PNG

---

##  Résultat  
Le graphique obtenu montre typiquement une **loi de puissance**, caractéristique des graphes de citations :  
![Graphique log/log](degree_distribution_loglog.png)

---

##  Exécution

### Option 1 :  Ouvrir dans Colab  
Clique pour ouvrir et exécuter le notebook en ligne :  
[![Ouvrir dans Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1tNObHmltkOzESvF7CiTExLgIgeaSBzUP)

### Option 2 :  Local (Python)
1. Cloner ce dépôt :
   ```bash
   git clone https://github.com/VOTRE_UTILISATEUR/VOTRE_REPO.git
