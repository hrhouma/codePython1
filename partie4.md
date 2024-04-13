# Classe `Personne` avec des paramètres explicatifs dans le constructeur

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

### Utilisation de la classe avec des noms de paramètres explicatifs

```python
# Création de l'objet personne avec des arguments explicites
p = Personne(aremplacerparnom="Dupont", aremplacerparprenom="Jean", aremplacerpartel="123456789", aremplacerparage=30)

# Appeler les méthodes
p.manger()
p.dormir()
```

### Explications

- Dans cet exemple, le constructeur de la classe `Personne` utilise des paramètres avec des noms explicatifs pour clarifier la fonction de chaque paramètre.
- Vous avez compris aussi comment les valeurs sont passées aux objets lors de leur création et comment ces valeurs sont utilisées pour initialiser les attributs de l'objet.
- Vous avez compris non seulement  comment les objets sont construits mais aussi vous avez saisi les concepts de la programmation orientée objet, en visualisant comment les données sont encapsulées au sein des objets.
