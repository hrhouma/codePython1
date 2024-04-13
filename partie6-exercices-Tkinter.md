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

**Exercice:**
Modifiez la fonction `choose_color` pour afficher la couleur choisie dans le terminal chaque fois qu'une couleur est sélectionnée. Utilisez `print()` pour afficher la valeur de la couleur.

Chaque exercice vous permet de pratiquer des modifications simples, renforçant votre compréhension de l'utilisation de Tkinter pour créer des interfaces utilisateur en Python. Ces activités vous encouragent également à explorer et à personnaliser davantage votre application.
