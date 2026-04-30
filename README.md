# Computational (Food) Systems Biology: Exercise 1

## Voraussetzungen

- [Quarto](https://quarto.org/docs/get-started/) >= 1.4
- Python >= 3.10 mit folgenden Paketen:

```bash
pip install -r requirements.txt
```

## Rendern

```bash
# Als Jupyter Notebook
quarto render ex1.qmd --to ipynb

# Als HTML
quarto render ex1.qmd --to html
```

## Struktur

```
ex1.qmd          # Hauptdatei (bindet alle Tasks ein)
task1/ … task11/ # Einzelne Aufgaben als .qmd
requirements.txt
```
