# Programmation orientée objet partie 3
### Étape 1: Création de la classe

Tout d'abord, nous commençons par définir la structure de base de notre classe sans aucun attribut ou méthode. Cela établit le "squelette" de notre classe.

```python
class Personne:
    pass
```

**Explication :**  
`class Personne:` définit une nouvelle classe nommée `Personne`. Le mot-clé `pass` est utilisé ici comme un remplisseur parce que le corps de la classe est encore vide. Cela permet de créer une classe sans générer d'erreurs.

### Étape 2: Ajout d'un constructeur

Ensuite, nous ajoutons un constructeur à la classe. Le constructeur est une méthode spéciale qui est appelée automatiquement lorsque vous créez un nouvel objet de cette classe.

```python
class Personne:
    def __init__(self):
        pass
```

**Explication :**  
`def __init__(self):` définit le constructeur de la classe. Le mot-clé `self` représente l'instance de la classe et permet d'accéder à ses attributs et méthodes.

### Étape 3: Définir des attributs dans le constructeur

Nous allons maintenant ajouter des attributs à notre classe. Ces attributs sont définis dans le constructeur, ce qui signifie qu'ils sont initialisés chaque fois qu'un objet de la classe est créé.

```python
class Personne:
    def __init__(self, aremplacerparnom, aremplacerparprenom, aremplacerpartel, aremplacerparage):
        self.nom = aremplacerparnom
        self.prenom = aremplacerparprenom
        self.tel = aremplacerpartel
        self.age = aremplacerparage
```

**Explication :**  
Chaque paramètre du constructeur (comme `aremplacerparnom`) est utilisé pour initialiser un attribut correspondant de l'objet (`self.nom`). `self.nom` stocke la valeur de `aremplacerparnom` pour l'objet spécifique.

### Étape 4: Ajout de méthodes

Ajoutons maintenant des méthodes à la classe pour définir les comportements.

```python
class Personne:
    def __init__(self, aremplacerparnom, aremplacerparprenom, aremplacerpartel, aremplacerparage):
        self.nom = aremplacerparnom
        self.prenom = aremplacerparprenom
        self.tel = aremplacerpartel
        self.age = aremplacerparage

    def manger(self):
        print(f"{self.prenom} mange.")

    def dormir(self):
        print(f"{self.prenom} dort.")
```

**Explication :**  
Les méthodes `manger` et `dormir` permettent à l'objet `Personne` de réaliser des actions. `self.prenom` dans les messages permet d'accéder à l'attribut `prenom` de l'objet pour personnaliser le message affiché.

### Étape 5: Création et utilisation d'objets

Enfin, nous allons créer un objet de la classe `Personne` et utiliser ses méthodes.

```python
# Création d'un objet Personne
personne1 = Personne("Dupont", "Jean", "123456789", 30)

# Utilisation des méthodes de l'objet
personne1.manger()
personne1.dormir()
```

**Explication :**  
`personne1` est un nouvel objet de type `Personne`, créé en passant des valeurs spécifiques au constructeur. Ensuite, nous appelons ses méthodes `manger` et `dormir` pour voir les actions effectuées par Jean.
