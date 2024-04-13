# Version Non Interactive

#### Étape 1 : Créer un Nouveau Fichier Python

1. **Ouvrir Visual Studio Code** : Lancez l'application.
2. **Créer un fichier** : Allez dans `File > New File`.
3. **Sauvegarder le fichier** : Enregistrez ce fichier sous le nom `restaurant.py` via `File > Save As...`.

#### Étape 2 : Définir la Classe `Restaurant`

1. **Taper le code de la classe** : Dans le fichier `restaurant.py`, commencez par écrire le code suivant pour définir la classe `Restaurant` avec deux attributs et deux méthodes.

```python
class Restaurant:
    def __init__(self, nom, cuisine_type):
        self.nom = nom
        self.cuisine_type = cuisine_type
    
    def decrire_restaurant(self):
        print(f"{self.nom} offre une excellente cuisine {self.cuisine_type}.")

    def ouvrir_restaurant(self):
        print(f"{self.nom} est maintenant ouvert.")
```

2. **Explication** : Les attributs `nom` et `cuisine_type` sont initialisés à travers le constructeur `__init__`. Les méthodes `decrire_restaurant` et `ouvrir_restaurant` permettent d'afficher des informations sur le restaurant et son statut.

#### Étape 3 : Créer et Tester une Instance de la Classe `Restaurant`

1. **Créer une instance** : À la fin du fichier `restaurant.py`, ajoutez le code pour créer une instance représentant votre restaurant préféré.

```python
# Création de l'instance de Restaurant
mon_restaurant = Restaurant("Chez Marco", "italienne")
```

2. **Utiliser les méthodes** : Utilisez les méthodes pour afficher les informations et le statut du restaurant.

```python
# Test des méthodes
mon_restaurant.decrire_restaurant()
mon_restaurant.ouvrir_restaurant()
```

#### Étape 4 : Exécuter le Script

1. **Ouvrir le terminal** : Dans Visual Studio Code, ouvrez un terminal via `Terminal > New Terminal`.
2. **Exécuter le fichier** : Tapez `python restaurant.py` dans le terminal et pressez `Enter` pour exécuter le script.

### Version Interactive

Pour rendre l'exercice interactif, modifiez le script pour permettre aux utilisateurs de définir les attributs du restaurant via des entrées utilisateur.

#### Étape 3 (Modifiée) : Demander des Entrées à l'Utilisateur et Créer une Instance

1. **Demander des entrées utilisateur** : Modifiez le fichier pour inclure des entrées utilisateur pour le nom et le type de cuisine.

```python
# Demande de saisie de l'utilisateur
nom = input("Entrez le nom du restaurant : ")
cuisine_type = input("Entrez le type de cuisine proposée : ")

# Création de l'instance de Restaurant
restaurant = Restaurant(nom, cuisine_type)
```

2. **Tester les méthodes** : Comme précédemment, utilisez les méthodes pour afficher les informations et le statut.

```python
# Test des méthodes
restaurant.decrire_restaurant()
restaurant.ouvrir_restaurant()
```

Vous pouvez suivre les mêmes étapes 4 et 1 pour exécuter et tester cette version interactive. 
