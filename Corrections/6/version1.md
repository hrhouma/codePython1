### Programme : Application de Dessin Simple avec Tkinter

#### Description du Programme
Ce programme offre une interface graphique simple permettant aux utilisateurs de dessiner avec la souris sur un canvas. Ils peuvent choisir différentes couleurs pour leur dessin et effacer le canvas s'ils le souhaitent. C'est une introduction amusante à la programmation GUI et à la gestion des événements en Python.

#### Code Python

```python
import tkinter as tk
from tkinter import colorchooser

def setup_canvas():
    """Configure le canvas pour le dessin."""
    canvas.bind('<B1-Motion>', draw)  # Dessiner quand le bouton gauche de la souris est pressé

def draw(event):
    """Dessine sur le canvas à la position de la souris."""
    x, y = event.x, event.y
    color = color_var.get()
    canvas.create_oval(x - 1, y - 1, x + 1, y + 1, fill=color, outline=color)

def clear_canvas():
    """Efface tous les dessins sur le canvas."""
    canvas.delete("all")

def choose_color():
    """Ouvre un dialogue pour choisir une couleur et met à jour la couleur active."""
    color = colorchooser.askcolor(title ="Choisir une couleur")
    if color:
        color_var.set(color[1])  # Met à jour la couleur sélectionnée

# Création de la fenêtre principale
root = tk.Tk()
root.title("Application de Dessin")

# Variables pour gérer les couleurs
color_var = tk.StringVar(value="black")  # Couleur de dessin par défaut

# Création d'un canvas pour le dessin
canvas = tk.Canvas(root, width=400, height=400, bg="white")
canvas.pack(pady=20)

# Boutons de contrôle
btn_frame = tk.Frame(root)
btn_frame.pack(fill=tk.X, ipady=5)

color_button = tk.Button(btn_frame, text="Choisir Couleur", command=choose_color)
color_button.pack(side=tk.LEFT, padx=10, fill=tk.X, expand=True)

clear_button = tk.Button(btn_frame, text="Effacer", command=clear_canvas)
clear_button.pack(side=tk.LEFT, padx=10, fill=tk.X, expand=True)

# Configuration du canvas
setup_canvas()

# Démarrage de l'application
root.mainloop()
```

#### Explication du Code
1. **Importations nécessaires** : Le programme utilise `tkinter` pour l'interface graphique et `colorchooser` pour un dialogue de sélection de couleur.
2. **Gestion du dessin** : Les fonctions `draw` et `setup_canvas` gèrent le dessin sur le canvas en utilisant les événements de la souris.
3. **Gestion de la couleur et effacement** : Les fonctions `choose_color` et `clear_canvas` permettent à l'utilisateur de choisir une couleur et d'effacer le canvas.
4. **Interface utilisateur** : L'interface comprend un canvas pour dessiner et des boutons pour choisir la couleur et effacer.

Ce programme offre une façon ludique de découvrir la programmation avec Python et peut servir de base pour des projets plus complexes, comme des applications de dessin plus avancées ou des jeux simples. 
# Instructions
1. Copier le code dans un fichier drawing_app.py
2. Exécutez python drawing_app.py
3. Amusez-vous à dessiner !
