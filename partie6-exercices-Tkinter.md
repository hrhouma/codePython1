# Exercice - reproduire l'application PAINT
### Code 1: Création de la Fenêtre Principale

Ce premier code est le squelette de base de toute application Tkinter. Il crée simplement une fenêtre principale.

```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()

# Démarre la boucle principale de l'application
root.mainloop()
```

### Code 2: Ajout d'un Titre à la Fenêtre

Ici, nous ajoutons un titre à la fenêtre principale pour donner plus de contexte à l'utilisateur sur ce que fait l'application.

```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()

# Ajout d'un titre à la fenêtre
root.title("Application de Dessin")

# Démarre la boucle principale de l'application
root.mainloop()
```

### Code 3: Ajout d'un Canvas pour Dessiner

Ce code introduit un `Canvas`, qui est l'espace où les utilisateurs pourront dessiner.

```python
import tkinter as tk

# Création de la fenêtre principale
root = tk.Tk()
root.title("Application de Dessin")

# Ajout d'un Canvas à la fenêtre
canvas = tk.Canvas(root, width=400, height=400, bg='white')
canvas.pack(pady=20)  # Ajoute un peu d'espace autour du canvas

# Démarre la boucle principale de l'application
root.mainloop()
```

### Code 4: Ajout d'un Bouton pour Choisir une Couleur

Ce morceau de code ajoute un bouton qui permet à l'utilisateur de choisir une couleur. Pour l'instant, le bouton ne fera rien jusqu'à ce que nous ajoutions la fonctionnalité dans un prochain exemple.

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

### Code 5: Fonctionnalité Complète du Bouton de Couleur

Nous allons maintenant faire en sorte que le bouton de couleur change réellement la couleur utilisée pour dessiner.

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

- Chaque étape introduit un nouvel élément ou une nouvelle fonctionnalité, vous aidant à comprendre progressivement comment construire une application avec une interface utilisateur en Python. 
- Vous pouvez continuer à construire sur cette base, en ajoutant des fonctionnalités comme la gestion des événements de dessin sur le canvas, l'ajout de plusieurs boutons pour différentes actions, etc.
