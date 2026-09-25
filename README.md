# Exos-Kholles
Tout élève de HX3 peut librement ajouter et partager ses exos de kholles

Il suffit de modifier directement le fichier .tex si vous ne savez pas utiliser github.

Chaque semaine possède son propre dossier contenant :

* le fichier source `.tex` 
* le PDF correspondant

Le fichier `preambule.tex` contient les packages, commandes et environnements LaTeX communs à toutes les semaines.

* Ajouter ou modifier un exercice:

1. Aller sur le dossier de la semaine correspondante.
2. Modifier l'exerice dans le fichier `.tex` correspondant.
3. Faire un commit avec un message explicite. (exemple: numéro des exos ajoutés ou nom de l'élève, etc)
4. Compiler si besoin le fichier afin de vérifier que le document fonctionne correctement.
5. Mettre à jour le PDF correspondant si possible.
6. Envoyer la branche sur GitHub.
7. Créer une Pull Request vers `main` si besoin.

Les modifications de `main` doivent passer par une Pull Request si besoin.

* Écriture des exercices

Les exercices utilisent les environnements et commandes définis dans `preambule.tex`.

Par exemple :

```latex
\begin{exercice}[Titre de l'exercice]
Énoncé de l'exercice.

\begin{questions}
    \item Première question.
    \item Deuxième question.
    \begin{questions}
        \item Première sous-question.
        \item Deuxième sous-question.
    \end{questions}
\end{questions}
\end{exercice}
```

Les fichiers auxiliaires générés lors de la compilation (`.aux`, `.log`, `.bbl`, etc.) ne doivent pas être ajoutés au dépôt.

* Travail collaboratif (si possible mais pas nécessaire)

Le dépôt utilise des branches et des Pull Requests afin d'éviter les modifications directes de `main`.

Avant de commencer à travailler, récupérer les dernières modifications de `main`.

Après avoir terminé :

```text
branche personnelle
       ↓
     commit
       ↓
      push
       ↓
Pull Request
       ↓
     review
       ↓
      main
```

* PDF

Les fichiers PDF sont conservés dans le dépôt afin que les exercices soient directement consultables sans avoir besoin de compiler les fichiers LaTeX.

* Fichiers à ne pas ajouter

Ne pas ajouter les fichiers générés automatiquement par LaTeX, notamment :

```text
*.aux
*.log
*.out
*.toc
*.fls
*.fdb_latexmk
*.synctex.gz
*.bbl
*.blg
*.bcf
*.run.xml
```

Ces fichiers sont automatiquement ignorés par Git grâce au `.gitignore`.
