# Guide Interactif pour Créer et Utiliser la Classe `Animal` avec Entrées Utilisateur

Ce tutoriel vous montre comment créer une classe `Animal` où vous pouvez entrer les données des animaux dynamiquement grâce à l'interaction utilisateur.

### Avant de Commencer
Assurez-vous que Python et Visual Studio Code sont installés sur votre ordinateur. Ouvrez Visual Studio Code pour commencer.

## Étape 1 : Créer un Nouveau Fichier Python

1. **Ouvrir Visual Studio Code** : Lancez l'application.
2. **Créer un fichier** : Allez dans `File > New File`.
3. **Sauvegarder le fichier** : Enregistrez ce fichier sous le nom `animal_interactif.py` via `File > Save As...`.

## Étape 2 : Définir la Classe `Animal`

1. **Taper le code de la classe** : Dans le fichier `animal_interactif.py`, commencez par écrire le code suivant pour définir la classe `Animal` avec des entrées utilisateur pour chaque attribut.

```python
class Animal:
    def __init__(self, nom, espece, age, son):
        self.nom = nom
        self.espece = espece
        self.age = age
        self.son = son
    
    def faire_du_bruit(self):
        print(f"{self.nom} dit: {self.son}")
```

2. **Explication** : Les attributs `nom`, `espece`, `age`, et `son` sont initialisés à travers le constructeur `__init__`. La méthode `faire_du_bruit` affiche le son caractéristique de l'animal.

## Étape 3 : Demander des Entrées à l'Utilisateur et Créer des Instances

1. **Demander des entrées utilisateur** : Ajoutez du code pour permettre à l'utilisateur de saisir les détails de l'animal.

```python
# Demande de saisie de l'utilisateur
nom = input("Entrez le nom de l'animal : ")
espece = input("Entrez l'espèce de l'animal : ")
age = int(input("Entrez l'âge de l'animal : "))
son = input("Quel son fait cet animal ? : ")

# Création de l'instance d'Animal
animal = Animal(nom, espece, age, son)
```

2. **Tester les méthodes** : Utilisez les méthodes pour afficher les informations et faire du bruit.

```python
# Affichage des informations et test de la méthode
print(f"{animal.nom} est un {animal.espece} et a {animal.age} ans.")
animal.faire_du_bruit()
```

3. **Explication** : L'utilisateur entre les données qui sont ensuite utilisées pour créer une instance de `Animal` et tester son comportement.

## Étape 4 : Exécuter le Script

1. **Ouvrir le terminal** : Dans Visual Studio Code, ouvrez un terminal via `Terminal > New Terminal`.
2. **Exécuter le fichier** : Tapez `python animal_interactif.py` dans le terminal et pressez `Enter` pour exécuter le script et suivre les instructions à l'écran.

## Conclusion

Vous avez maintenant appris à créer une classe en Python qui prend en compte les entrées de l'utilisateur pour initialiser ses attributs. Cette méthode interactive rend l'apprentissage de la programmation plus engageant et illustre comment les programmes peuvent interagir avec les utilisateurs en temps réel.
