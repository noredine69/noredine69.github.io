---
layout: post
title:  "Normalisation des messages de commits"
date:   2022-12-13 16:00:00 +0100
categories: dev
abstract: Comment améliorer la traçabilité de votre code, et la lisibilité de votre arbre git.
---
### Intro
Qui ne s'est jamais posé cette question, en regardant un arbre git "mais à quoi ça correspond" ?
Et bien, je vais vous présenter comment répondre en partie à cette question, ou plutôt comment
mettre en place des mécanismes pour éviter d'analyser du code datant de plus de 6 mois.

### Pré-requis
Il faut que vous utilisiez un outil de ticketing, de type Jira, où chaque fonctionnalité, ou bug est identifié
par un numéro unique. Aussi, il faut avoir accès à tous les postes de dev, et obviously utiliser Git comme 
gestionnaire de code source (non mais qui utilise encore svn ici ?).

### Installation
L'outil principal à installer est `pre-commit`, comme son nom l'indique il permet de configurer les hooks de Git.
Un git hook est un script executé selon la nature de l'évènement git, par ex. le script `pre-commit` sera executé avant le commit. L'autre outil à installer est `gitlint`, qui va gérer les règles des messages de commit.

Les commandes à executer : 
```
    sudo apt install python3-pip -y
    pip3 install pre-commit gitlint
```

### Configuration
A la racine de chaque projet :
- Ajout d'un hook de type `commit-msg` :
```
    pre-commit install --hook-type commit-msg 
```
- Initialisation du fichier de configuration `pre-commit` :
```
    pre-commit sample-config > .pre-commit-config.yaml 
```
Modifier le fichier afin qu'il soit de la forme :

```
default_language_version:
    python: python3.8
default_stages: [commit]
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.4.0
    hooks:
    -   id: trailing-whitespace
    -   id: end-of-file-fixer
    -   id: check-yaml
    -   id: check-added-large-files
-   repo: https://github.com/jorisroovers/gitlint
    rev: v0.12.0
    hooks:
    -   id: gitlint
```

Les outils  `trailing-whitespace`, `end-of-file-fixer`, `check-yaml` et `check-added-large-files` sont ajoutés par défaut,
à vous de voir si vous souhaitez les conserver.

Il ne reste qu'à configurer `gitlint`, via le fichier `.gitlint` :

```
[general]
ignore=body-is-missing,body-first-line-empty,title-trailing-punctuation
debug=true

[title-max-length]
line-length=200

[title-must-not-contain-word]
words=

[title-match-regex]
regex=^(\[((US|TS|BUG|PI|JIRA)-[0-9]*|RELEASE)\]\s[a-zA-Z_])|(WIP)

[body-min-length]
min-length=3
```

Le plus important ici c'est la fameuse regex, qui va forcer les messages de commits de type "[US-123456]" tout en autorisant
"WIP".

