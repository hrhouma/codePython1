# Exercice 1: Classe Animal

**Description :**  
Créez une classe `Animal` qui représente les informations de base d'un animal.

**Attributs :**  
- `nom` (le nom de l'animal)
- `espece` (l'espèce de l'animal)
- `age` (l'âge de l'animal)

**Méthodes :**  
- `faire_du_bruit()` qui affiche un son caractéristique de l'animal.

**Test :**  
Instanciez un animal de votre choix, définissez ses attributs et faites-le "faire du bruit".

---


D'accord, je vais ajuster le guide pour inclure le son comme un attribut de la classe `Animal`, qui sera passé comme paramètre lors de la création de chaque instance. Cette approche rend le modèle plus flexible et permet aux étudiants de comprendre l'utilisation des attributs personnalisés lors de l'instanciation.

---

# Correction Étape par Étape pour Créer et Utiliser la Classe `Animal`

Dans ce tutoriel, nous allons créer une classe `Animal` qui intègre des attributs pour le nom, l'espèce, l'âge, et un son caractéristique. Chaque instance de la classe pourra utiliser ces attributs pour simuler des comportements.

### Avant de Commencer
Assurez-vous que Python et Visual Studio Code sont installés sur votre ordinateur. Ouvrez Visual Studio Code pour commencer.

## Étape 1 : Créer un Nouveau Fichier Python

1. **Ouvrir Visual Studio Code** : Lancez l'application.
2. **Créer un fichier** : Allez dans `File > New File`.
3. **Sauvegarder le fichier** : Enregistrez ce fichier sous le nom `animal.py` via `File > Save As...`.

## Étape 2 : Définir la Classe `Animal`

1. **Taper le code de la classe** : Dans le fichier `animal.py`, commencez par écrire le code suivant pour définir la classe `Animal` avec un attribut supplémentaire pour le son.

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

2. **Explication** : Les attributs `nom`, `espece`, `age`, et `son` sont initialisés à travers le constructeur `__init__`. La méthode `faire_du_bruit` utilise l'attribut `son` pour afficher un son caractéristique de l'animal.

## Étape 3 : Créer et Tester des Instances de la Classe `Animal`

1. **Créer des instances** : À la fin du fichier `animal.py`, ajoutez le code pour créer plusieurs instances d'`Animal`, chacune avec un son unique.

```python
# Création de différentes instances d'Animal
simba = Animal("Simba", "lion", 3, "egrrrrrrrrrrrr!")
milo = Animal("Milo", "chat", 1, "miawwwwww!")
```

2. **Définir les attributs et tester les méthodes** : Testez les comportements sonores en appelant la méthode `faire_du_bruit`.

```python
# Affichage des informations et test des méthodes
print(f"{simba.nom} est un {simba.espece} et a {simba.age} ans.")
simba.faire_du_bruit()
print(f"{milo.nom} est un {milo.espece} et a {milo.age} ans.")
milo.faire_du_bruit()
```

3. **Explication** : Les informations de chaque animal sont affichées, et leur son spécifique est émis grâce à la méthode `faire_du_bruit`.

## Étape 4 : Exécuter le Script

1. **Ouvrir le terminal** : Dans Visual Studio Code, ouvrez un terminal via `Terminal > New Terminal`.
2. **Exécuter le fichier** : Tapez `python animal.py` dans le terminal et pressez `Enter` pour exécuter le script.

## Conclusion

Vous avez appris à créer une classe en Python avec des attributs personnalisés, y compris un attribut pour un son spécifique. Ce modèle illustre comment utiliser la programmation orientée objet pour simuler des comportements réalistes et dynamiques en informatique.



