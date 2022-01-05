# TLN-Analyse-de-sentiments
Analyse de polarité de mots dans des commentaires avec SVM 

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#data"> Data </a></li>
      </ul>
      <ul>
        <li><a href="#results"> Results </a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
L'objectif de ce projet est de créer un modèle capable de prédire au mieux la polarité d'un mot dans une phrase. 
Cette polarité peut prendre les valeur positive, neutre ou négative. 

### Data
Il y a deux dossiers dans ce repo GIT car il y a deux fichiers à étudier :
* des commentaires de restaurants
* des commentaires d'ordinateurs

Les features utilisées sont : 
* term : le terme à étudier (dont on doit prédire la polarité)
* text : la phrase complète dans laquelle se trouve le terme
* senti word : les mots retenus connu de sentiword pour l'analyse
* score by word : le score pour chaque mot connu de sentiword (le score peut etre vide, par exempe "le" n'a pas de polarité)
* pos tag : les posTag obtenu à partir de la tokenization

La variable à prédire :
* polarity : la polarité du term auquelle elle est associée

### Results
Les meilleurs résultats obtenus sont les suivants et le détails et les explications de chaque traitement se trouve dans les Jupyter Notebook :

**LAPTOP**
Training time: 1.282226s; Prediction time: 0.018031s
positive:  {'precision': 0.9032258064516129, 'recall': 0.9655172413793104, 'f1-score': 0.9333333333333333, 'support': 29}
negative:  {'precision': 0.9333333333333333, 'recall': 0.875, 'f1-score': 0.9032258064516129, 'support': 16}
neutral:  {'precision': 1.0, 'recall': 0.75, 'f1-score': 0.8571428571428571, 'support': 4}

**RESTAURANT**
Training time: 3.793309s; Prediction time: 0.067593s
positive:  {'precision': 0.8933333333333333, 'recall': 0.9852941176470589, 'f1-score': 0.9370629370629371, 'support': 68}
negative:  {'precision': 1.0, 'recall': 0.6666666666666666, 'f1-score': 0.8, 'support': 18}
neutral:  {'precision': 0.8888888888888888, 'recall': 0.8, 'f1-score': 0.8421052631578948, 'support': 10}



