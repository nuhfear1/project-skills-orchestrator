# Workflow phases

Ce document définit les phases canoniques du Project Skills Orchestrator.

## Principes

- Une phase ne doit pas être sautée sans justification explicite.
- Les ressources conseillent ; l’orchestrateur synthétise ; l’utilisateur valide.
- Le développement ne commence pas tant que la porte `DESIGN_VALIDATED` n’est pas ouverte.
- Toute écriture dans un dépôt, installation, publication ou déploiement nécessite une autorisation explicite.
- Une validation porte sur un livrable précis.

## Phase 0 — Cadrage

Objectif : transformer l’idée en brief exploitable.

Livrables : objectif, publics, positionnement, promesse, contraintes, contenu, critères de réussite.

Porte : `BRIEF_VALIDATED`.

## Phase 1 — Recherche et direction

Objectif : explorer les références, les options d’expérience, les contraintes techniques et les ressources adaptées.

Livrables : benchmark, directions créatives, architecture d’expérience, shortlist de ressources.

Porte : `DIRECTION_VALIDATED`.

## Phase 2 — Structure et wireframes

Objectif : définir le parcours, la hiérarchie de contenu et les interactions essentielles.

Livrables : sitemap, user flow, wireframes, modèle de contenu multilingue.

Porte : `WIREFRAMES_VALIDATED`.

## Phase 3 — Design system et maquettes

Objectif : fixer l’identité visuelle, les composants et les états interactifs.

Livrables : design system, maquettes haute fidélité, règles responsive, motion direction.

Porte : `DESIGN_VALIDATED`.

## Phase 4 — Architecture technique

Objectif : traduire les décisions validées en architecture de réalisation.

Livrables : stack, structure du dépôt, stratégie 3D, animation, i18n, accessibilité, performance et tests.

Porte : `ARCHITECTURE_VALIDATED`.

## Phase 5 — Implémentation

Objectif : produire le projet par incréments vérifiables.

Livrables : code, tests, documentation et prévisualisations.

Porte : `IMPLEMENTATION_VALIDATED`.

## Phase 6 — Revue et lancement

Objectif : vérifier qualité, accessibilité, performance, sécurité, contenu et déploiement.

Porte : `RELEASE_APPROVED`.

## États de porte

- `NOT_STARTED`
- `IN_PROGRESS`
- `BLOCKED`
- `BRIEF_VALIDATED`
- `DIRECTION_VALIDATED`
- `WIREFRAMES_VALIDATED`
- `DESIGN_VALIDATED`
- `ARCHITECTURE_VALIDATED`
- `IMPLEMENTATION_VALIDATED`
- `RELEASE_APPROVED`
