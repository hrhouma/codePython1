# partie1-Guide Étape par Étape pour la Classe Personne.md

Ce guide vous aidera à comprendre comment la classe `Personne` est construite et utilisée en Python. Suivez les étapes pour apprendre à définir des attributs, des méthodes, et à créer des instances de la classe.

## Étape 1: Définition de la Classe

### Code
```python
class Personne:
    nom = "Briand"
    prenom = "Pierre-Luc"
    tel = "(438)445-5544"
    age = 20
```

### Explication
- **Attributs de Classe** : `nom`, `prenom`, `tel`, et `age` sont définis avec des valeurs par défaut. Ces valeurs sont partagées par toutes les instances de la classe sauf si elles sont redéfinies.

## Étape 2: Ajout du Constructeur

### Code
```python
    def __init__(self, parametre1, parametre2):
        self.nom = parametre1
        self.prenom = parametre2
```

### Explication
- **Constructeur** : `__init__` est une méthode spéciale qui est appelée quand une nouvelle instance de la classe est créée. `parametre1` et `parametre2` sont utilisés pour initialiser `nom` et `prenom` de l'instance.

## Étape 3: Définition des Méthodes

### Code
```python
    def manger(self):
        print("Je mange lasagne")

    def dormir(self):
        print("Je dors tard")
```

### Explication
- **Méthodes** : `manger` et `dormir` sont des actions que chaque instance de la classe peut exécuter. Ces méthodes affichent des messages simples quand elles sont appelées.

## Étape 4: Création d'Instances et Utilisation

### Code
```python
a = Personne("REHOUMA", "Haythem")
print(a.nom + " " + a.prenom)

b = Personne("CUNHA", "Nastasia")
print(b.nom + " " + b.prenom)
```

### Explication
- **Création d'Instances** : `a` et `b` sont des instances de `Personne`. Leurs attributs `nom` et `prenom` sont initialisés avec les valeurs spécifiées lors de la création.
- **Affichage des Attributs** : On utilise `print` pour afficher le `nom` et le `prenom` de chaque instance, démontrant que les valeurs par défaut ont été remplacées par celles fournies au constructeur.

## Conclusion

- La classe `Personne` démontre les bases de la programmation orientée objet en Python, y compris la définition de la classe, le constructeur, les méthodes, et la création d'instances.
- Chaque étape est conçue pour renforcer la compréhension de ces concepts essentiels.

# Tous le code 
Ce bloc comprend la définition de la classe `Personne`, la création d'instances de cette classe, et l'affichage des attributs de ces instances :

```python
class Personne:
    # Attributs de classe avec des valeurs par défaut
    nom = "Briand"
    prenom = "Pierre-Luc"
    tel = "(438)445-5544"
    age = 20

    # Constructeur avec paramètres pour nom et prénom
    def __init__(self, parametre1, parametre2):
        self.nom = parametre1
        self.prenom = parametre2

    # Méthode pour simuler l'action de manger
    def manger(self):
        print("Je mange lasagne")

    # Méthode pour simuler l'action de dormir
    def dormir(self):
        print("Je dors tard")

# Création de l'instance 'a' avec des noms personnalisés
a = Personne("REHOUMA", "Haythem")
print(a.nom + " " + a.prenom)  # Affichage des attributs de l'instance 'a'

# Création de l'instance 'b' avec d'autres noms personnalisés
b = Personne("CUNHA", "Nastasia")
print(b.nom + " " + b.prenom)  # Affichage des attributs de l'instance 'b'
```

- Ce code complet est prêt à être utilisé dans une leçon ou inclus dans des documents pédagogiques pour enseigner les concepts de base de la programmation orientée objet en Python.
- Il montre comment définir une classe, initialiser ses instances avec des valeurs spécifiques, et comment utiliser ces instances pour appeler des méthodes et afficher des informations.



# Instructions Étape par Étape pour la Classe `Personne` en Python

### Avant de Commencer
Assurez-vous d'avoir installé Python et Visual Studio Code sur votre ordinateur. Ouvrez Visual Studio Code pour commencer.

## Instruction 1 : Créer un Nouveau Fichier Python

1. **Créer un fichier** : Ouvrez Visual Studio Code, allez dans le menu `File > New File`.
2. **Sauvegarder le fichier** : Sauvegardez ce fichier avec l'extension `.py`, par exemple `personne.py`, en allant dans `File > Save As...`.

## Instruction 2 : Définition de la Classe

1. **Écrire le code de la classe** : Dans votre fichier `personne.py`, commencez par définir la classe `Personne` avec des attributs par défaut.

```python
class Personne:
    nom = "Briand"
    prenom = "Pierre-Luc"
    tel = "(438)445-5544"
    age = 20
```

2. **Explication** : Les attributs `nom`, `prenom`, `tel`, et `age` sont des valeurs par défaut partagées par toutes les instances de la classe.

## Instruction 3 : Ajouter un Constructeur à la Classe

1. **Modifier la classe** : Ajoutez le constructeur `__init__` pour initialiser les instances avec des valeurs spécifiques.

```python
    def __init__(self, parametre1, parametre2):
        self.nom = parametre1
        self.prenom = parametre2
```

2. **Explication** : Le constructeur `__init__` est utilisé pour créer des instances de la classe avec des noms et prénoms spécifiques.

## Instruction 4 : Ajouter des Méthodes à la Classe

1. **Écrire des méthodes** : Ajoutez des méthodes `manger` et `dormir` qui permettent à l'instance de réaliser des actions.

```python
    def manger(self):
        print("Je mange lasagne")

    def dormir(self):
        print("Je dors tard")
```

2. **Explication** : Ces méthodes permettent d'afficher des activités de la personne.

## Instruction 5 : Créer des Instances et les Utiliser

1. **Écrire le code pour créer des instances** : À la fin de votre fichier, créez des instances et utilisez-les.

```python
a = Personne("REHOUMA", "Haythem")
print(a.nom + " " + a.prenom)

b = Personne("CUNHA", "Nastasia")
print(b.nom + " " + b.prenom)
```

2. **Explication** : `a` et `b` sont des instances de la classe `Personne`. Les attributs sont initialisés avec les valeurs fournies.

## Instruction 6 : Exécuter le Script

1. **Ouvrir le terminal** : Dans Visual Studio Code, ouvrez un terminal en allant dans `Terminal > New Terminal`.
2. **Exécuter le fichier** : Tapez `python personne.py` dans le terminal et appuyez sur `Enter`.




## Instruction 7 : Créer et Utiliser des Instances

1. **Créer des instances** : En bas de votre fichier, ajoutez le code pour créer plusieurs instances et les utiliser.

```python
# Instances de la classe Personne
a = Personne("REHOUMA", "Haythem")
b = Personne("CUNHA", "Nastasia")
c = Personne("MARTIN", "Elise")
d = Personne("DUPONT", "Alexandre")

# Affichage des noms
print(a.nom + " " + a.prenom)
print(b.nom + " " + b.prenom)
print(c.nom + " " + c.prenom)
print(d.nom + " " + d.prenom)

# Appel des méthodes
a.manger()
b.dormir()
c.manger()
d.dormir()
```

2. **Explication** : Ce code crée quatre instances de `Personne` et utilise les méthodes pour afficher des comportements.

# Instruction 8 :Exécuter le Script

1. **Ouvrir le terminal** : Dans Visual Studio Code, ouvrez un terminal via `Terminal > New Terminal`.
2. **Exécuter le fichier** : Dans le terminal, tapez `python personne.py` et pressez `Enter` pour voir les résultats.



## Conclusion

Ce guide démontre les bases de la programmation orientée objet en Python, incluant la définition de classes, le constructeur, les méthodes, et la création d'instances. Suivez chaque étape pour renforcer votre compréhension et appliquer ces concepts.
