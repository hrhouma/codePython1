# Étape 1: Création de la classe de base sans constructeur

Dans cette première version, la classe `Personne` contiendra des attributs de base et des méthodes simples. Nous n'utiliserons pas encore de constructeur, donc les attributs devront être définis après la création de l'objet.

```python
class Personne:
    # Attributs de classe
    nom = "Nom par défaut"
    prenom = "Prénom par défaut"
    tel = "0000000000"
    age = 0

    def manger(self):
        print(f"{self.prenom} mange.")

    def dormir(self):
        print(f"{self.prenom} dort.")
```

### Utilisation de la classe

```python
# Création de l'objet personne
p = Personne()
# Définir les attributs
p.nom = "Dupont"
p.prenom = "Jean"
p.tel = "123456789"
p.age = 30

# Appeler les méthodes
p.manger()
p.dormir()
```

### Explications

Dans cet exemple, la classe `Personne` ne possède pas de constructeur (`__init__`). Cela signifie que les attributs de chaque objet `Personne` doivent être explicitement définis après sa création. Cette approche peut entraîner des erreurs si on oublie de définir certains attributs, et elle n'est pas très pratique pour gérer plusieurs objets de type `Personne`.

### Étape 2: Ajout du constructeur

Maintenant, ajoutons un constructeur à la classe `Personne` pour initialiser les attributs lors de la création de l'objet.

```python
class Personne:
    def __init__(self, nomaremplacer, prenomaremplacer, telaremplacer, agearemplacer):
        self.nom = nomaremplacer
        self.prenom = prenomaremplacer
        self.tel = telaremplacer
        self.age = agearemplacer

    def manger(self):
        print(f"{self.prenom} mange.")

    def dormir(self):
        print(f"{self.prenom} dort.")
```

### Utilisation de la classe avec constructeur

```python
# Création de l'objet personne avec le constructeur
p = Personne("Dupont", "Jean", "123456789", 30)

# Appeler les méthodes
p.manger()
p.dormir()
```

### Explications

Dans cette version, la classe `Personne` utilise un constructeur `__init__` pour initialiser les attributs d'un objet lors de sa création. Cela rend le code plus sûr et plus facile à maintenir car les attributs doivent être fournis lors de la création de l'objet, évitant ainsi les oublis et garantissant que l'objet est toujours dans un état complet et valide.

### Conclusion

L'utilisation d'un constructeur dans une classe permet de s'assurer que tous les objets créés à partir de cette classe sont initialisés avec tous les attributs nécessaires, réduisant les risques d'erreur et simplifiant la gestion des objets dans le code. Cela illustre l'un des avantages clés de la programmation orientée objet : la capacité de modéliser des entités avec des structures de données et des comportements bien définis.
