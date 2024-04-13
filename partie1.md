# Guide Étape par Étape pour la Classe `Personne`

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
