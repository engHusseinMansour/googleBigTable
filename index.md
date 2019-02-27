---
titre: Google Cloud Big table et API JAVA 
description: Tutoriel pour les débutants sur google big table
---
## Tutoriel de Google Cloud Big table

BigTable est un système de gestion de base de données compressées, haute performance, propriétaire, développé et exploité par [Google](https://www.google.com).

C'est une base de données orientée colonnes, dont se sont inspirés plusieurs projets libres, comme HBase, Cassandra ou Hypertable.

Chez Google, BigTable est stockée sur le système de fichiers distribué GoogleFS.

Google ne distribue pas sa base de données mais propose une utilisation publique de BigTable via sa plateforme d'application Google App Engine.
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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
