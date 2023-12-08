# WebScraping

Automatiser la collecte des produits du site [ACTION](https://www.action.com/fr-fr/).

## Notes

- 50% sur le continue (evaluation orale sur le code)
- 50% sur le SAE

## Evaluation continue

Evaluation du code Python permettant de collecter de manière automatique tous les produits d'une catégorie en les sauvegardants au format JSON
- Le code s'execute sans erreurs
- Le code récupère les produits de toutes les pages d'une catégorie (ie: habitat)
- Le code écrit en JSON toutes les informations détaillées
- Le groupe est capable de naviguer dans le code et d'expliquer précisement chaque étape
- Le groupe connaît les mots clefs du WebScraping en Python (API, requête, réponse, Front ..)

## SAE

### I - Structure du code

#### Programmation fonctionnelle

Chaque groupe veillera a rendre son code python en respectant les standards de code des développeurs Python en programmation fonctionnelle. 
Pour se faire le groupe organisera le code en fonctions, chacune ayant une tâche spécifique. Utilisez des noms de fonctions descriptifs dans une seule langue (Français ou Anglais).

Soyez cohérent, il faut que chaque nom de variable puisse décrire le contenu (pas de variable `i`, `j` etc..)

Ceci est juste un exemple :

```python
from datetime import date

def any_function(firstname: str, lastname: str) -> str:
  """Example"""
  return f"Hello {firstname} {lastname}"

def my_other_function() -> date:
  today_date = date.today()
  return today_date

if __name__ "__main__":
  sentence_str = any_function("xavier", "lai")
  today_date = my_other_function()
  print(f"{today_date}\n{sentence_str}"
```

#### Typage

Le groupe typera son code Python. Le typage permet aux developpeurs de lire plus rapidemment le code et de comprendre le type de chaque variable, argument, retour de fonction et constantes.

Pour typer on utilise le module [`typing`](https://www.pythontutorial.net/python-basics/python-type-hints/) qui est natif dans Python.

```
from typing import List, Dict

def extract_data(url: str) -> List[Dict[str, str]]:
  """Typed function example"""
    #This function takes a url argument that is a str, and returns a List of Dictionnaries where the key is a str and the value is a str

def clean_data(data: List[Dict[str, str]]) -> List[int]:
  pass
```

#### Commentaires

Le groupe ajoutera uniquement les commentaires pertinents lorsque le code est compliqué (pas trop de commentaires)

#### ReadMe

Ajouter un fichier `README.md` qui est un markdown contenant l'explication du projet.

### II - Analyse des produits Action

1. Terminer le `TD process json`. Vous devez donc avoir un Pandas DataFrame contenant une ligne pour chaque produit. Ecrivez ce DataFrame en format `xlsx` avec la méthode `to_excel()`.
2. Sortez des statistiques sur les produits que vous avez collectés (nombre de produits, distribution du prix, moyenne des promotions etc ..)

RENDU : Le groupe transmettra donc son code Python structuré, l'excel contenant les produits venant du Pandas DataFrame, ainsi qu'un Jupyter Notebook ou un script.py permettant de calculer les statistiques.

contact : xavier.lai.pro@gmail.com
