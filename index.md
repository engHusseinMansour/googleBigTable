---
titre: Google Cloud Big table et API JAVA 
description: Tutoriel pour les débutants sur google big table
---
# Tutoriel de Google Cloud Big table

## Introduction :
BigTable est un système de gestion de base de données compressées, haute performance, propriétaire, développé et exploité par [Google](https://www.google.com). C'est une base de données orientée colonnes, dont se sont inspirés plusieurs projets libres, comme HBase, Cassandra ou Hypertable.

## Le Public :

Ce didacticiel s'adresse à tous les professionnels du logiciel qui souhaitent apprendre à utiliser la BigTable en étapes simples et faciles, il vous donnera une bonne compréhension générale des concepts de Google BigTable.

## Avant de commencer :

1. Sélectionnez ou créez un projet GCP :
    1. Passez au page [Gérer les ressources](https://console.cloud.google.com/cloud-resource-manager?hl=ar&_ga=2.213750932.-1032159468.1550254809&_gac=1.217784738.1551279192.EAIaIQobChMI3oOPnJXc4AIV7ZXtCh0ACgRYEAAYASAAEgJNWPD_BwE), choisissez l'organisation puis créer un nouveau projet, ici je choisis  *"myfirstTest"* (Voir le video)
    4. Activer les API Cloud Bigtable et Cloud Bigtable Admin (Voir le video)

Créer un nouveau projet:

[![Créer un nouveau projet](http://img.youtube.com/vi/aJSMdPDHg7w/0.jpg)](http://www.youtube.com/watch?v=aJSMdPDHg7w)

Activer les API :

[![Créer un nouveau projet](http://img.youtube.com/vi/TyGEHFj6h9c/0.jpg)](http://www.youtube.com/watch?v=TyGEHFj6h9c)
## Démarrage rapide :

Pour vous connecter à une instance Cloud Bigtable, effectuer des tâches administratives basiques, et lire et écrire des données dans une table, On a deux options :
1. **Commande cbt :** est une interface de ligne de commande permettant d'effectuer différentes opérations sur Cloud Bigtable. Il est écrit en Go à l'aide de la bibliothèque cliente Go pour Cloud Bigtable, pour plus des informations [commande cbt](https://cloud.google.com/bigtable/docs/cbt-overview?hl=fr)
2. **Système HBase :** est un système de gestion de base de données non-relationnelles distribué, écrit en Java, disposant d'un stockage structuré pour les grandes tables, pour plus des informations [Système HBase](https://hbase.apache.org/).


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll ISSAE Cnam Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ISSAE/ISSAE.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

Exemple of _config.yml

```yml
remote_theme: ISSAE/architect

name: Programmation Avancée 

author: Pascal Fares

author_email: pascal.fares@isae.edu.lb

title: Programmation Avancée et Patron de conception en Java

google_analytics: UA-29708002-2

repository: ISSAE/NFP121

plugins:
  - jekyll-sitemap
  - jekyll-seo-tag
```


### For reviewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

0. [Get jekyll](https://jekyllrb.com/docs/installation/windows/)

1. Clone down the theme's repository (`git clone https://github.com/ISSAE/architect.git`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
   4.1. Si votre projet n'est pas un theme ajouter un fichier [Gemfile](https://github.com/ISSAE/NFP121/blob/master/Gemfile) qui resemble à celui ci [https://github.com/ISSAE/NFP121/blob/master/Gemfile](https://github.com/ISSAE/NFP121/blob/master/Gemfile)
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
