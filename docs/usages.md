# À quoi servent les workflows ?

Les workflows permettent d'automatiser des tâches répétitives dans
un projet. Voici les usages les plus courants :

## Lancer des tests automatiquement

À chaque fois qu'on pousse du code, le workflow peut lancer tous
les tests du projet pour vérifier que rien n'est cassé.

## Déployer un site

C'est exactement ce qu'on fait dans ce TP ! À chaque push, le workflow
déploie automatiquement le site sur GitHub Pages.

## Vérifier la qualité du code

Un workflow peut analyser le code et signaler les erreurs de style
ou les mauvaises pratiques (on appelle ça du "linting").

## Compiler un projet

Pour les projets qui nécessitent une compilation (Java, C++...),
le workflow peut compiler automatiquement à chaque modification.

## Publier une nouvelle version

Quand on crée une nouvelle release, le workflow peut automatiquement
publier le package sur npm, PyPI, etc.