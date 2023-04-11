---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.13.8
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

# Jupyter Notebooks


## Edit Mode vs. Cell Mode

- **Edit Mode**: grün angewählt + Cursor sichtbar

- **Cell Mode**: blau angewählt;
    - Möglichkeit zur Navigation zwischen den Zellen
    - `Y`: turn into code cell
    - `M`: turn into Markdown cell
    - `A`: insert cell above
    - `B`: insert cell below
    
## Cell types

- Markdown Cell
    - [resource zu Markdon Syntax](https://www.markdownguide.org/basic-syntax)
- Code Cell
    - `Cmd+Enter`: execute cell
    - `Shift+Enter`: execute cell and move to next

## Notebook extensions

--> [Anleitung zur Installation](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html)

- evtl. nützliche Auswahl
    - reveal
    - Markdown preview
    - Table of Contents

## Code

```python
print('hello notebook')
```

	hello notebook