# Project Skills Orchestrator

Dépôt central et canonique pour auditer, classer et orchestrer des **skills**, **bibliothèques** et **outils** utilisés dans les projets numériques.

## Rôle

- sélectionner les ressources adaptées à chaque phase ;
- conserver les skills originaux intacts ;
- appliquer des règles externes d’autorité, de sécurité et de conflit ;
- empêcher le passage prématuré au développement ;
- centraliser les audits et décisions ;
- fournir aux futurs projets une source unique et versionnée.

## Structure

```text
.
├── SKILL.md
├── audits/
├── policies/
├── project-profiles/
├── references/
├── registry/
└── templates/
```

## Ressources actuellement enregistrées

### Skills

- UI/UX Pro Max — approuvé sous contrôle — 8,0/10
- GSAP AI Skills — approuvé avec overrides — 8,4/10

### Bibliothèques

- Motion — bibliothèque officielle optionnelle — 9,1/10 comme bibliothèque

### Outils

- 21st.dev — activation à la demande, limitée au dépôt et à l’environnement du projet

## Règle de gestion

Ce dépôt est la **source de vérité**. Les mises à jour se font par commits dans ce même dépôt. Les ZIP ne sont réservés qu’aux installations initiales ou aux jalons importants.

## Utilisation dans un projet

Le projet cible peut installer ou référencer cet orchestrateur depuis GitHub, puis consulter ses registres pour décider quels skills, bibliothèques et outils activer.

Aucun secret, jeton API ou donnée de production ne doit être stocké ici.
