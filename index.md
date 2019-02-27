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

1. Sélectionnez ou créez un projet GCP : (Voir les videos)
    1. Passer au page [Gérer les ressources](https://console.cloud.google.com/cloud-resource-manager?hl=ar&_ga=2.213750932.-1032159468.1550254809&_gac=1.217784738.1551279192.EAIaIQobChMI3oOPnJXc4AIV7ZXtCh0ACgRYEAAYASAAEgJNWPD_BwE), choisir l'organisation puis créer un nouveau projet, par exemple  *"myfirstTest"*.
    2. Activer les API Cloud Bigtable et Cloud Bigtable Admin.
    3. Créer un identifiant pour accéder à vos API activées.

**Créer un nouveau projet:**

[![Créer un nouveau projet](http://img.youtube.com/vi/aJSMdPDHg7w/0.jpg)](http://www.youtube.com/watch?v=aJSMdPDHg7w)

**Activer les API :**

[![Créer un nouveau projet](http://img.youtube.com/vi/TyGEHFj6h9c/0.jpg)](http://www.youtube.com/watch?v=TyGEHFj6h9c)

Tous les APIs :

![APIs](https://lh3.googleusercontent.com/tP4PVh2R14ObkFZ9Md_m3p4Bp0vqBn_yONq6lqVckCaCMxbq4gh97sL8EODUs_wNj067BxZcucQdn-IJ6pB09LB3cD4LcX6NgSAzSy9Zcr0GwXqOxtm3LoX94C4HWmfgwmOs65of=w1080-h477-no)

**Créer un identifiant :**

[![Créer un identifiant](http://img.youtube.com/vi/gUHj7UXUjjw/0.jpg)](http://www.youtube.com/watch?v=gUHj7UXUjjw)

## Activer la facturation pour votre projet :

![Etape 1](https://lh3.googleusercontent.com/CuClptU3uOP7m9w34nHHt4zb8Hk3C11CBosMBZfiQerX4miVasLV31U2r34qLyDfkEmp_y_CU2GX8KYQ5Yv2K9qV-7CWohAVIg1IzL14g8LWp6YLuJ4u60jM-d4vFsN15DVuHB83IXhAU8huqs6qa4dK5rdpGgNYrhfao-b__AsHjgrpgJEe9C_m85bBOiAPTJsKCJEFebPD8T2ZVRt49LjFFtx8Z-WxD8iCNO6XmAsVtcq9n0jl5UKlRUh5UY8K2jdlNDzrgmUf9ASDBEzIiwVSBWWUngGjOwKZcLcI8DgsdbzpiYfPJu7iKvT9EQ83s6aJchIt1UyOyqsevSYrRhtieD4cnG-xN1v7J7uGkQEelJQroBlWfZG2osI3OLMZllU6YlFEipqcU8Ge7vnwwRv65De3y2O0YbUU8ZmEP85eHg8W7JkXsu8cUzhIrtibyRqH68fJgnhkP0XsOFa1qj8I0caL-Fvv5fIf-uIux8vzBszWX4Kpx4jYeMMwfgOfGqUMnIHq5WTDslb7kr_VtDnG2g8NHhtGJOGMr4P4lEtfXJZ_6pDV_G-9eBXVJfBctfd6TALx-S9mJUy8ErFCoA2aiwRuSAQkdtKa0w-CYYa2vi27i9SERgrVlOjXJTpFvmdv-TzF52yug54WM3-CH8MjnxA87oJkLjzUL_kUinFjCZE995nb9SyAhF8KbDZFbS0E0LSwcGRe6WWkcC1rUDo=w1440-h818-no)

![Etape 2](https://lh3.googleusercontent.com/2Z8J_WlWnrXvmzmiXQcydmIY4Y5dgfZieNgJ3RdTdPlJUvrcnG1_LStmAaEZ71NkuE5LA6Nt5hZwyxHOcsZk18Y8vOhxNzSQUXkEM4xlf-Sc7BSOVr1c0bPJkR3DIFrDXYori1civQb38OFJnonQYW-LR7u1s_XaVoqWPkkdkkjuV5YyTigUfqcevXAse9roVDmNJ7iQi28GqHv0IJUOs2GhHf5kYoY6fo6GNrW5YwXErHsuHYowQOCQ6XB4wzZdOjdlyEN8s20DtDPA0dg4M0MI-4CZGVFK4UgfXJuPjX0yTQ79AyXs5FLQ3QUVsIt1FMmC8ptpuIzZbDn-FS_CaZsqJC3HzKNlnHc84xP044NKHsUzVrGJFRCCaSWfeXpQEaFwqXk0ba4pf1vNSHHG9Lp143OLSVuOpKzh3AOsC4MgjWfbDK1QvgZjGQjGmxtqgck9YHvQlqfPaC8ANnge5nkpecGrDeB6Ik-W0TmkRIyx-X4D-6nO4WdYL_mfHZCcgDRxbOXcMNSnMQ8c_QVQG2PRmqx7LwskWjeXOtVJAEnd-eDDLwEXfvbWjGW3vT2eLBGZRQN-Pgs4n28w4vhmozMAr6V62l9-jDVJWX0jLZZQqtFLdOEe4mmTwN_gNPjoMvcvvPT2xpC_igNFT1rJN50SJTww1J_pe-FdYzSAdHNZlLHg7K8y-xO8v0VVUcF0ahWZPXtu6IpCCvAr7u19zVc=w1440-h820-no)

## Créer une instance :
[Voir la documentation](https://cloud.google.com/bigtable/docs/creating-instance)
 
![New Instance](https://cloud.google.com/bigtable/img/create-instance.png)

## Démarrage rapide :

Pour vous connecter à une instance Cloud Bigtable, effectuer des tâches administratives basiques, et lire et écrire des données dans une table, On a deux options :
1. **Commande cbt :** est une interface de ligne de commande permettant d'effectuer différentes opérations sur Cloud Bigtable. Il est écrit en Go à l'aide de la bibliothèque cliente Go pour Cloud Bigtable, pour plus des informations [commande cbt](https://cloud.google.com/bigtable/docs/cbt-overview?hl=fr)
2. **Système HBase :** est un système de gestion de base de données non-relationnelles distribué, écrit en Java, disposant d'un stockage structuré pour les grandes tables, pour plus des informations [Système HBase](https://hbase.apache.org/).


## Exemple de JAVA API :
Nous allons utiliser HBase pour appliquer un exemple **API HBase pour Java "Hello World" Application**

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
