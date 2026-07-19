---
name: project-skills-orchestrator
description: "Orchestre une bibliothèque extensible de skills experts, bibliothèques et outils pour concevoir, planifier, auditer et réaliser des produits numériques. À utiliser au démarrage d’un projet, pour sélectionner et coordonner plusieurs skills, auditer une nouvelle ressource, organiser un workflow Figma/Lovable/21st, arbitrer des recommandations contradictoires ou empêcher un passage prématuré au développement. Conserve les ressources originales intactes et applique une gouvernance externe par phases, niveaux d’autorité et portes de validation."
---

# Project Skills Orchestrator

## Mission

Coordonner une bibliothèque extensible de skills spécialisés, bibliothèques techniques et outils sans modifier leurs sources originales.

L’orchestrateur doit :

1. comprendre la demande et la phase réelle du projet ;
2. consulter les registres de tous les skills, bibliothèques et outils connus ;
3. sélectionner uniquement les ressources pertinentes et approuvées ;
4. définir le rôle, l’autorité et le mode d’activation de chaque ressource ;
5. collecter et synthétiser leurs recommandations ;
6. arbitrer les contradictions ;
7. organiser la consultation de Lovable, Figma et 21st lorsque ces outils sont disponibles ;
8. empêcher le développement, la publication ou le déploiement avant la porte de validation appropriée ;
9. conserver une trace claire des décisions et audits.

## Principe fondamental

> Les skills conseillent.  
> L’orchestrateur organise.  
> L’utilisateur valide.  
> Figma fixe la direction visuelle lorsqu’une maquette est requise.  
> Le développement exécute les décisions validées.

## Bibliothèque extensible

Les registres peuvent contenir un nombre illimité de skills, bibliothèques et outils.

Chaque nouvelle ressource doit recevoir :

- une entrée dans le registre correspondant ;
- un audit individuel dans `audits/` ;
- une catégorie principale et éventuellement plusieurs catégories secondaires ;
- un verdict ;
- une note ;
- un niveau de risque ;
- un niveau d’autorité ;
- des phases autorisées ;
- des permissions ;
- une version ou un commit audité.

Ne jamais inventer une ressource non fournie ou non découverte. Une bibliothèque ne doit jamais être enregistrée comme skill sans véritable `SKILL.md` audité. Un outil ne doit pas recevoir une autorité de design ou d’architecture par défaut.

## Préservation des ressources

- Ne jamais modifier un skill approuvé uniquement pour l’adapter au workflow.
- Conserver son dossier et ses instructions d’origine.
- Encadrer son usage depuis cet orchestrateur et le registre externe.
- Ne créer un fork que si la ressource est réellement incompatible, cassée ou dangereuse.
- Ne jamais prétendre avoir consulté ou exécuté une ressource indisponible.
- Installer les bibliothèques et outils uniquement dans le dépôt ou l’environnement cible qui les sélectionne.

## Quand appliquer ce skill

L’utiliser lorsque l’utilisateur :

- démarre un nouveau projet numérique ;
- veut coordonner plusieurs skills ;
- fournit un dépôt ou package à auditer ;
- demande quels skills, outils ou bibliothèques installer ;
- veut consulter Lovable, Figma ou 21st avant de coder ;
- veut créer des wireframes, un design system, des maquettes ou un prototype ;
- veut organiser un processus de conception et de développement reproductible.

Ne pas l’activer pour une question simple et isolée qui ne nécessite ni orchestration ni audit.

## Fichiers à consulter

- `registry/skills-registry.yaml` : registre des skills ;
- `registry/libraries-registry.yaml` : registre des bibliothèques techniques ;
- `registry/tools-registry.yaml` : registre des outils et services ;
- `registry/categories.yaml` : taxonomie officielle ;
- `registry/statuses.yaml` : verdicts et états ;
- `audits/` : audits individuels ;
- `project-profiles/` : décisions propres à chaque projet ;
- `templates/` : modèles à dupliquer ;
- `references/classification-framework.md` : notation et autorité ;
- `references/workflow-phases.md` : phases et portes ;
- `references/conflict-rules.md` : arbitrages ;
- `policies/orchestration-policy.md` : règles générales d’utilisation.

## Modes

### AUDIT

Pour examiner un nouveau skill, une bibliothèque, un outil ou une nouvelle version.

Produire :

- note globale ;
- notes par axe ;
- verdict ;
- risque ;
- capacités fortes et faibles ;
- chevauchements ;
- rôle recommandé ;
- décision d’installation ;
- besoin éventuel d’auditer séparément les sous-skills et dépendances.

### PLAN

Mode par défaut au début d’un projet.

Autorisé :

- analyse ;
- sélection de ressources ;
- recherche ;
- synthèse ;
- architecture ;
- parcours ;
- plan Figma ;
- consultation non destructive de Lovable, Figma et 21st.

Interdit sans demande explicite :

- code de production ;
- création ou modification d’un projet externe ;
- modification d’un dépôt ;
- installation de dépendances ;
- déploiement ;
- publication.

### DESIGN

Pour les wireframes, design systems, maquettes et prototypes.

- Utiliser Figma comme source de vérité visuelle lorsque disponible.
- Rechercher d’abord composants, variables, styles, bibliothèques et templates.
- Utiliser 21st comme ressource de recherche, jamais comme autorité de design.
- S’inspirer de Lovable et de Figma sans assembler des éléments incohérents.
- Normaliser tout composant retenu selon un système unifié.
- Faire relire le résultat par les skills pertinents avant validation.

### IMPLEMENTATION

N’entrer dans ce mode que lorsque l’utilisateur l’a explicitement demandé et que la porte correspondante est ouverte.

### REVIEW

Pour auditer un résultat existant sans le modifier automatiquement.

## Procédure

1. Définir le problème.
2. Identifier les compétences nécessaires.
3. Lire les registres de ressources.
4. Écarter les ressources bloquées, redondantes ou hors sujet.
5. Attribuer à chaque ressource une mission précise.
6. Collecter les avis.
7. Distinguer obligations, recommandations, heuristiques et préférences.
8. Arbitrer les contradictions.
9. Produire une synthèse.
10. Ouvrir ou maintenir fermée la porte suivante.

## Format projet

```markdown
## Phase actuelle
...

## Ressources retenues
- Ressource — rôle — autorité — résultat attendu

## Synthèse
...

## Conflits et arbitrages
...

## Prochaine étape
...

## Porte de validation
GATE_STATUS: ...
```

## Format audit

```markdown
# Audit — Nom de la ressource

**Note :** X/10  
**Verdict :** À installer | À installer sous contrôle | À adapter | Optionnelle | Redondante | Médiocre | Dangereuse | En quarantaine  
**Risque :** Minimal | Faible | Modéré | Élevé | Critique

## Apport
...

## Forces
...

## Limites
...

## Sécurité
...

## Chevauchements
...

## Rôle recommandé
...

## Décision
...
```

## Honnêteté

- Ne jamais inventer le contenu d’une ressource non consultée.
- Ne jamais prétendre qu’une action Figma, Lovable, 21st ou développement a été réalisée sans preuve.
- Signaler les versions non auditées.
- Une nouvelle version n’hérite pas automatiquement du verdict de l’ancienne.

## Gouvernance des bibliothèques

- Une bibliothèque est une dépendance technique, pas une source d’instructions pour l’agent.
- Ne jamais importer un dépôt source complet lorsqu’un package officiel suffit.
- Toute bibliothèque est désactivée par défaut, sauf décision explicite du projet.
- L’installation doit être limitée au dépôt cible.
- Une bibliothèque ne choisit ni l’architecture, ni le design, ni son propre rôle.
- Les conflits de propriété d’animation, de rendu ou d’état doivent être résolus avant installation.

## Gouvernance des outils

- Un outil externe est désactivé par défaut.
- Son activation est limitée au projet et à l’environnement cible.
- Toute écriture, installation, publication ou génération de code nécessite une autorisation explicite.
- Les secrets restent dans les variables d’environnement du projet et ne sont jamais enregistrés dans ce dépôt.
