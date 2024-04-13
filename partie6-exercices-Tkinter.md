# Exercice - reproduire l'application PAINT

### Étape 1: Création de la Fenêtre Principale

**Code Initial:**
```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()

# Démarre la boucle principale de l'application
root.mainloop()
```

**Exercice:**
Modifiez la taille de la fenêtre principale pour qu'elle soit 800 pixels de large par 600 pixels de haut.

### Étape 2: Ajout d'un Titre à la Fenêtre

**Code Initial:**
```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()

# Ajout d'un titre à la fenêtre
root.title("Application de Dessin")

# Démarre la boucle principale de l'application
root.mainloop()
```

**Exercice:**
Changez le titre de la fenêtre en "Mon Application de Dessin".

### Étape 3: Ajout d'un Canvas pour Dessiner

**Code Initial:**
```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()
root.title("Application de Dessin")

# Ajout d'un Canvas à la fenêtre
canvas = tk.Canvas(root, width=400, height=400, bg='white')
canvas.pack(pady=20)

# Démarre la boucle principale de l'application
root.mainloop()
```

**Exercice:**
Changez la couleur de fond du canvas en gris clair (`lightgray`).

### Étape 4: Ajout d'un Bouton pour Choisir une Couleur

**Code Initial:**
```python
import tkinter as tk
from tkinter import colorchooser

# Création de la fenêtre principale
root = tk.Tk()
root.title("Application de Dessin")

# Ajout d'un Canvas
canvas = tk.Canvas(root, width=400, height=400, bg='white')
canvas.pack(pady=20)

# Fonction pour choisir une couleur
def choose_color():
    colorchooser.askcolor()

# Ajout d'un bouton pour changer la couleur
color_button = tk.Button(root, text="Choisir Couleur", command=choose_color)
color_button.pack(fill=tk.X)

# Démarre la boucle principale de l'application
root.mainloop()
```

**Exercice:**
Ajoutez un autre bouton intitulé "Effacer le dessin" qui, pour le moment, ne fera rien. Positionnez ce bouton à côté du bouton "Choisir Couleur".

### Étape 5: Fonctionnalité Complète du Bouton de Couleur

**Code Initial:**
```python
import tkinter as tk
from tkinter import colorchooser

# Création de la fenêtre principale
root = tk.Tk()
root.title("Application de Dessin")

# Ajout d'un Canvas
canvas = tk.Canvas(root, width=400, height=400, bg='white')
canvas.pack(pady=20)

# Variable pour stocker la couleur actuelle
current_color = 'black'

# Fonction pour choisir une couleur
def choose_color():
    global current_color
    color = colorchooser.askcolor()[1]
    if color:
        current_color = color

# Ajout d'un bouton pour changer la couleur
color_button = tk.Button(root, text="Choisir Couleur", command=choose_color)
color_button.pack(fill=tk.X)

# Démarre la boucle principale de l'application
root.mainloop()
```


# Correction Détaillée avec Commentaires

# Correction de l'Étape 1: Modification de la Taille de la Fenêtre

**Code Commenté:**
```python
import tkinter as tk  # Importe le module tkinter pour créer l'interface graphique

# Création de la fenêtre principale
root = tk.Tk()  # Crée l'objet principal de la fenêtre, appelé root
root.geometry("800x600")  # Définit la taille de la fenêtre à 800x600 pixels

# Démarre la boucle principale de l'application
root.mainloop()  # Lance la boucle événementielle qui attend les interactions de l'utilisateur
```

# Correction de l'Étape 2: Changement du Titre de la Fenêtre

**Code Commenté:**
```python
import tkinter as tk  # Importe le module tkinter

# Création de la fenêtre principale
root = tk.Tk()  # Crée l'objet fenêtre principal, root

# Ajout d'un titre à la fenêtre
root.title("Mon Application de Dessin")  # Définit le titre de la fenêtre

# Démarre la boucle principale de l'application
root.mainloop()  # Lance la boucle d'exécution qui permet à la fenêtre de rester ouverte
```

# Correction de l'Étape 3: Changement de la Couleur de Fond du Canvas

**Code Commenté:**
```python
import tkinter as tk  # Importation du module tkinter

# Création de la fenêtre principale
root = tk.Tk()  # Instanciation de la fenêtre principale
root.title("Application de Dessin")  # Mise en place du titre de la fenêtre

# Ajout d'un Canvas à la fenêtre avec une couleur de fond modifiée
canvas = tk.Canvas(root, width=400, height=400, bg='lightgray')  # Crée un canvas avec fond gris clair
canvas.pack(pady=20)  # Ajoute le canvas à la fenêtre avec un padding vertical

# Démarre la boucle principale de l'application
root.mainloop()  # Commence la boucle événementielle de tkinter
```

# Correction de l'Étape 4: Ajout d'un Autre Bouton

**Code Commenté:**
```python
import tkinter as tk  # Importation de tkinter pour l'interface graphique
from tkinter import colorchooser  # Importation du sélecteur de couleur

# Création de la fenêtre principale
root = tk.Tk()  # Création de l'objet root qui est la fenêtre principale
root.title("Application de Dessin")  # Attribution d'un titre à la fenêtre

# Ajout d'un Canvas
canvas = tk.Canvas(root, width=400, height=400, bg='white')  # Création du canvas de dessin
canvas.pack(pady=20)  # Placement du canvas dans la fenêtre avec un espace vertical

# Fonction pour choisir une couleur
def choose_color():
    colorchooser.askcolor()  # Ouvre la boîte de dialogue pour choisir une couleur

# Ajout d'un bouton pour changer la couleur
color_button = tk.Button(root, text="Choisir Couleur", command=choose_color)  # Crée un bouton pour la sélection de couleur
color_button.pack(side=tk.LEFT, fill=tk.X, expand=True)  # Positionne le bouton à gauche, étendu sur l'axe X

# Ajout d'un bouton pour effacer le canvas (ne fait rien pour le moment)
clear_button = tk.Button(root, text="Effacer le dessin")  # Crée un second bouton pour effacer le dessin
clear_button.pack(side=tk.LEFT, fill=tk.X, expand=True)  # Positionne ce bouton à côté du bouton de couleur

# Démarre la boucle principale de l'application
root.mainloop()  # Lance la boucle principale pour rendre la fenêtre interactive
```

# Correction de l'Étape 5: Affichage de la Couleur Choisie dans le Terminal

**Code Commenté:**
```python
import tkinter as tk  # Importation de tkinter
from tkinter import colorchooser  # Importation du module colorchooser pour la sélection de couleur

# Création de la fenêtre principale
root = tk

.Tk()  # Instanciation de la fenêtre principale
root.title("Application de Dessin")  # Mise en place du titre de la fenêtre

# Ajout d'un Canvas
canvas = tk.Canvas(root, width=400, height=400, bg='white')  # Création d'un canvas blanc pour dessiner
canvas.pack(pady=20)  # Ajout du canvas à la fenêtre avec un espace vertical

# Variable pour stocker la couleur actuelle
current_color = 'black'  # Définit la couleur initiale pour dessiner

# Fonction pour choisir une couleur
def choose_color():
    global current_color  # Permet de modifier la variable globale current_color
    color = colorchooser.askcolor()[1]  # Ouvre la boîte de dialogue et retourne la couleur choisie
    if color:
        current_color = color  # Met à jour la couleur actuelle
        print("Couleur sélectionnée:", current_color)  # Affiche la couleur choisie dans le terminal

# Ajout d'un bouton pour changer la couleur
color_button = tk.Button(root, text="Choisir Couleur", command=choose_color)  # Crée un bouton pour changer la couleur
color_button.pack(fill=tk.X)  # Ajoute le bouton à la fenêtre, étendu sur l'axe X

# Démarre la boucle principale de l'application
root.mainloop()  # Commence la boucle événementielle pour rendre l'application interactive
```

**Exercice:**
Modifiez la fonction `choose_color` pour afficher la couleur choisie dans le terminal chaque fois qu'une couleur est sélectionnée. Utilisez `print()` pour afficher la valeur de la couleur.

Chaque exercice vous permet de pratiquer des modifications simples, renforçant votre compréhension de l'utilisation de Tkinter pour créer des interfaces utilisateur en Python. Ces activités vous encouragent également à explorer et à personnaliser davantage votre application.
