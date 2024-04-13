```python
class Animal:
    nom = ''
    espece = ''
    age = 0
    son = ''

    def __init__(self, paramnom, paramespece, paramage, paramson):
        self.nom = paramnom
        self.espece = paramespece
        self.age = paramage
        self.son = paramson

    def faire_du_bruit(self):
        print(f"{self.nom} dit: {self.son}")

# Création de différentes instances d'Animal
simba = Animal("Simba", "lion", 3, "egrrrrrrrrrrrr!")
milo = Animal("Milo", "chat", 1, "miawwwwww!")

print(simba.faire_du_bruit())
print(milo.faire_du_bruit())


# Demande de saisie de l'utilisateur
nom1 = input("Entrez le nom de l'animal : ")
espece1 = input("Entrez l'espèce de l'animal : ")
age1 = int(input("Entrez l'âge de l'animal : "))
son1 = input("Quel son fait cet animal ? : ")

lola = Animal(nom1, espece1, age1, son1)
print(lola.faire_du_bruit())
```
