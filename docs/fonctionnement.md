# Comment fonctionnent les workflows ?

## Structure d'un workflow

Un workflow est un fichier **YAML** (`.yml`) placé dans le dossier
`.github/workflows/` de ton dépôt.

Il est composé de 3 éléments principaux :

### 1. Le déclencheur (`on`)
C'est ce qui active le workflow. Par exemple :
- `push` : à chaque push sur le dépôt
- `pull_request` : quand une Pull Request est ouverte
- `schedule` : à une heure programmée (comme une cron job)

### 2. Les jobs
Un job est un groupe de tâches qui s'exécutent sur une machine virtuelle.
On peut avoir plusieurs jobs qui tournent en parallèle.

### 3. Les steps
Ce sont les étapes à l'intérieur d'un job. Chaque step exécute
une commande ou une action.

## Exemple concret

```yaml
name: Deploy
on: push

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Récupérer le code
        uses: actions/checkout@v3

      - name: Déployer
        run: echo "Déploiement en cours..."
```

## Les intérêts des workflows

- **Gain de temps** : plus besoin de faire les tâches à la main
- **Fiabilité** : le robot ne fait pas d'erreurs d'étourderie
- **Rapidité** : les problèmes sont détectés immédiatement
- **Collaboration** : toute l'équipe bénéficie des mêmes vérifications