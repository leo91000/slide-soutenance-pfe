---
theme: seriph
background: /antennes-orange.jpg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Page de couverture soutenance
name: Page de garde
title: Page de garde
---

<div class="flex flex-row items-center justify-center">
  <img src="/orange.png" class="h-20 rounded shadow d-block mr-5" />
  <img src="/imt.png" class="h-20 bg-white rounded shadow d-block ml-5" />
</div>

# Conception et développement de l'outil DOE
### Soutenance de PFE par Léo Coletta

<Pagination />

<style>
h1 {
  @apply mt-10;
}
</style>

<!--
Bonjour,

Dans le cadre de mon projet de fin d'étude à Orange, j'ai conçu et développé l'outil DOE ; un outil facilitant le dépôt et le contrôle documentaire.

Ce projet d'envergure s'inscrit dans une période de transition chez Orange avec le projet Towerco, et il m'a fallu faire preuve de beaucoup d'agilité afin de mener à bien ce projet.

Petit avertissement : Je ne vais pas rentrer dans tous les détails techniques des points abordés, n'hésitez pas à me poser des questions à la fin si vous voulez plus de détail.
-->

---
layout: two-cols
name: Sommaire
---

<Header />

<AbsoluteTitle :level="1">Sommaire</AbsoluteTitle>

<div class="mt-18"></div>

1. L'entreprise Orange
2. Les enjeux de l'application
    - Le processus de déploiement des sites
    - Les DOE
    - Historique
3. La solution DOE Web
    - Pourquoi une version Web ?
    - Présentation de l'outil
    - Présentation technique
    - Méthodologie du projet
3. Le projet de transformation Towerco
    - Description du projet
    - Cession de la documentation
    - Adaptation de l'outil DOE
4. Résultats & Pistes de réflexion

::right::

<div class="mt-8 h-full flex flex-column items-center justify-center">
  <img src="/antenne-orange-2.jpg" class="h-80 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Avant de vous expliquer les tenants et les aboutissants du projet, je vais donner quelques rappels sur Orange.

Afin de mieux comprendre le projet, je vais expliquer le contexte avec la première en version en Excel puis le projet Towerco.

Ensuite, je vais expliquer plus en détails le projet que j'ai développer : l'outil DOE en version web. Je vais expliquer l'utilité de l'outil, la méthodologie du projet mais aussi les outils techniques utilisés

Pour terminer, j'expliquerai tous les enseignements que j'ai tirer de ce PFE, ainsi qu'une réflexion sur mon expérience.
-->

---
layout: two-cols
name: Présentation de Orange
---

<Header />

<AbsoluteTitle :level="1">Présentation de l'entreprise Orange</AbsoluteTitle>

<div class="mt-30"></div>

- Opérateur de Télécommnunications
- 42,2 milliards € de chiffres d'affaires
- 147 000 employés
- Solutions B2B & B2C
- Leader historique sur le marché
- 1<sup>er</sup> opérateur mobile pour la 10<sup>ème</sup> année consécutive selon l'ARCEP

::right::

<div class="h-full flex flex-column items-center justify-center">
  <img src="/orange.png" class="h-80 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Comme vous le savez, Orange est un opérateur de télécommunication dans les offres les plus connus sont les offres mobiles et les offres fibres. Néanmoins Orange exerce beaucoup d'autres activités. On peut citer par exemple :
 - Orange Bank
 - Orange Cyberdefense
 - Orange Business Service

Sur le marché des télécommunications, c'est un leader historique qui conserve son titre de 1er opérateur mobile selon l'Arcep depuis 10 ans.

ARCEP = Autorité de régulation des communications électroniques, des postes et de la distribution de la presse

Commentaires :
Décrire ce que s'est l'ARCEP

Commentaires :
Non pas tous le monde connait Orange

Nombre d'employé / CA

Vous connaissez !probablement (par X, par Y)
Pourquoi Orange est si connu ?
-->

---
layout: two-cols
name: Présentation de mon département
---

<Header />

<AbsoluteTitle :level="1">Zoom sur mon département</AbsoluteTitle>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/upr-ne.png" class="h-80 d-block mx-auto" />
</div>


::right::

<div class="mt-25" />

- L'<u>**Unité de Pilotage Réseau**</u>
  - IRM (Ingénierie Réseau Mobile)
  - OPR (Opération Performance Réseau mobile)
  - APR (Anticipation Programmation Réseau Fixe)
  - <u>**DEP (Déploiement Réseau Mobile)**</u>
    - Conception et Négoication Sites Mobiles
    - Pilotage Production Mobile Nord Est
    - <u>**Performances Relations Bailleurs**</u>
    - ...
  - ...

<Pagination />

<!--
J'ai effectué mon alternance à l'UPR l'unité de pilotage réseau dont l'objectif est de déployer et maintenir un réseau de qualité.

Plus spécifiquement, j'étais dans l'entité DEP (Déploiement Réseau Mobile) qui, comme son nom l'indique s'occupe du déploiement du réseau mobile

Plus spécifiquement, j'étais dans l'équipe PRB (Performance Relation bailleur) qui s'occupe de gérer les relations avec les bailleurs des sites antennaires d'Orange.

Commentaires :
L'entreprise Orange et pas Orange
Zoom sur mon département
C'est un groupe international

A des entités dans toute la France,
-->

---
layout: cover
name: Les enjeux de l'application
background: /background-contexte.jfif
---

# Les enjeux de l'application

---
layout: two-cols
name: Processus de déploiement des sites mobiles
---

<Header />

<AbsoluteTitle :level="1">Les enjeux de l'application</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Le processus de déploiement des site mobiles</AbsoluteTitle>

<div class="mt-30" />

- Marketing : cible à atteindre (4G, 5G, etc)
- Validation en fonction des budgets
- Etude du besoin (hauteur du pylone, installations, etc)
- Négociation et signature du bail
- Travaux de construction

::right::

<img src="/antenne-orange.jpg" class="h-60 mt-25 rounded shadow d-block mx-auto" />

<Pagination />

---
layout: two-cols
name: Qu'est ce qu'un DOE ?
---

<Header />

<AbsoluteTitle :level="1">Les enjeux de l'application</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Qu'est ce qu'un DOE ?</AbsoluteTitle>

<div class="mt-40" />

- DOE = <span class="font-bold">D</span>ossier d'<span class="font-bold">O</span>uvrage <span class="font-bold">E</span>xécuté
- A l'issue des travaux réalisés sur sites, des documents sont nécessaires
- Initialement 300+ documents fournis à chaque opération

::right::

<img src="/documentation.png" class="h-38 mt-40 rounded shadow d-block mx-auto" />

<Pagination />

<!--
Avant de rentrer plus dans le détails l'outil, il est nécessaire de comprendre ce qu'un un DOE.

Le processus de déploiement comprends diverses étapes :
- La négociation
- La construction

A l'issue des travaux réaliser sur un site mobile Orange, une documentation doit être fournis. Ces documents sont soit d'ordre légal, soit utiles à la maintenance des sites.

Orange fait appel à des prestataires pour installer les sites mobiles. Il faut donc réclamer et contrôler la fourniture des documents.

Initialement cette tâche était très complexe, et par soucis de simplicité plus de 300 documents étais fournis à chaque opération.

Commentaire :
- Se mettre plus en valeur
-->

---
layout: two-cols
name: Historique
---

<Header />

<AbsoluteTitle :level="1">Les enjeux de l'application</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Outil DOE Version Excel</AbsoluteTitle>

<div class="mt-40" />

- Automatiser la documentation des travaux réalisés sur site
- Outil initialement développé sur Excel
- Suivi des DOES traités par boîte mail

::right::

<div class="h-full flex flex-column items-center justify-center">
  <img src="/doe-excel-profil-ame.png" class="h-60 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Je vais à présent vous expliquez le contexte de l'outil DOE.

Ayant pour objectif de réduire les nombre de documents à fournir et d'assurer un suivi des DOE, l'outil DOE version Excel  a vu le jour et a été utilisé pendant de nombreuses années.
-->

---
layout: cover
name: Fonctionnalités de l'application
background: /background-fonctionnalites.jfif
---

# La solution DOE Web

<!--
Je vais à présent vous expliquer le fonctionnement de l'application.
-->

---
layout: two-cols
name: Pourquoi version WEB ?
---

<Header />

<AbsoluteTitle :level="1">La solution DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Pourquoi une version WEB ?</AbsoluteTitle>

<div class="mt-20" />

- Simplifier l'expérience utilisateur
  - Interface utilisateur intuitive
  - Limiter le nombre de clics pour contrôler les DOE
  - Simplifier les processus
  - Limiter le nombre d'outil nécessaire au contrôle d'un DOE
- Répondre aux limitations de VBA
  - Archivage de toutes les données (S3)
  - Interconnexion aux applications du SI Orange
  - Réduire les temps de traitement
  - Décomplexifier le suivi (boîte mail en VBA)
  - Problématique de sécurité
  - Automatiser ce qui est impossible/compliqué en VBA
    - Connexion à BDE Site
    - Push SFTP
- Augmenter la sécurisation des données (RGPD)

::right::

<div class="h-full flex flex-column items-center justify-center px-10">
  <img src="/web.jpg" class="w-full rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Notre équipe a décidé de passer l'outil DOE pour plusieurs raisons :
- Améliorer l'expérience utilisateurs avec des interfaces utilisateurs intuitives. Sans connaitre le processus entier de déploiement du réseau mobile, un utilisateur doit être capable d'utiliser l'outil.
- Limiter le nombre de clics pour contrôler le DOE et permettre d'accélerer la fourniture
- Limiter un maximum le nombre d'outil tierce à utiliser pour fonctionner   (aujourd'hui, un amenageur doit utiliser 3 et 5 outils différents en même temps pour fournir un DOE)

Au dela de l'amélioration de l'expérience utilisateur, une version WEB permet de répondre à beaucoup de limitation du VBA :
- En version WEB le déploiement de l'application est instantanné, sur l'outil Excel cela nécessite une communication aux 5 UPR qui elle même sont chargés de transmettre l'outil.
- L'interconnexion au SI d'Orange peut être abstrait à l'utilisateur en version WEB, alors qu'en version excel il doit utiliser les différents outils du SI.
- Réduire les temps de traitement
- Simplifier la gestion du suivi qui se faisait en boite mail

Enfin, un outil Excel ne peut pas répondre à la problématique de sécurisation des données RGPD. Une version WEB peut implémenter beaucoup plus facilement les techniques anonymisation ou de cryptage des données.

Commentaires :

Décrire RGPD,
L'ancienne version ne respectait pas la RGPD
Si l'entreprise
La solution excel n'était plus adapté aux besoin de l'entreprise
-->

---
layout: two-cols
name: feat | Création du DOE
clicks: 2
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Création du DOE</AbsoluteTitle>

<div class="mt-23" />

- Améliorations vs Excel
    - Formulaire plus intuitif
    - Auto complétion des champs du formulaire
    - Beaucoup plus performant

<hr class="my-5 mr-4">

- Renseignement des informations sur l'opération
    - Code opération
    - Type d'opération
    - Bandes de fréquence
    - Recetteur
    - ...
- Plus d'options : Génération des cases à cocher
    - Détails plus spécifiques
    - Généré en fonction du type d'opération

::right::

<ZoomableImage src="/app/fonctionnalite-nouveau-suivi-doe.png" :zoomed-x="-220" :zoomed-y="-20" :scale="1.7" class="mt-25 rounded shadow" />=

<Pagination />

<!--
La création du DOE est l'étape de renseignement de l'opération. L'utilisateur fait part des détails du DOE comme par exemple le type de l'opération ou les bandes de fréquences.

Après cette étape, l'outil génère un certains nombre de cases à cocher afin d'avoir plus de détails sur l'opération.

Une fois le formulaire complété, l'utilisateur peut créer son DOE

Commentaire:
- Sur chaque slide donner les avantages, ce qu'on a valu changer, ce qui ne fonctionnait pas, ce qu'on a voulu améliorer

Commentaire :
Expliquer mieux les cases à cocher
- Dans la soltiion, un certain nombre d'informations optionnels sont générés en cliquant sur générer cases à cocher
-->

---
layout: two-cols
name: feat | Dépot / Contrôle
preload: false
clicks: 2
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Dépôt/Contrôle des documents</AbsoluteTitle>

<div class="mt-23" />

- Améliorations vs Excel
    - Une saisie facilitée
    - Les fichiers sont analysé progressivement
    - Plus performant
    - Plus fiable

<hr class="my-5 mr-4">

- Fichiers attendus générés automatiquement
- Fourniture Obligatoire / Conditionnelle
- Fichiers fournis assignés aux fichiers attendus correspondant
- Fichier OK ou NOK ou Fourniture ultérieur
- Outil de renommage automatique à une règle donnée


::right::

<ZoomableImage src="/app/fonctionnalite-controle-des-documents.png" :zoomed-x="-240" :zoomed-y="-35" :scale="2.1" class="ml-5 mt-35 rounded shadow" />

<Pagination />

<!--
Après cette étape, l'utilisateur se retrouve sur la phase de dépôt des documents. A l'aide du formulaire remplis précédemment, l'outil génère un certain nombre de documents attendus. L'utilisateur doit donc déposer ses documents avec un le même nommage pour que l'outil détecte qu'il a été fournis.

Sur cette page, à également accès à :
- une visionneuse de documents
- un outil de renommage qui permet de renommer un documents automatiquement à la bonne règle de nommage.
- le dictionnaire que j'expliquerai dans la slide suivante

Après cette étape l'utilisateur soumet son DOE à validation, et le documentaliste ou le bureau de contrôle va étudier les pièces fournis pour contrôler leurs validité. Le DOE peut être refusé, validé, validé avec complément ou validé sans contrôle.

Commentaires :
- Ralentir le débit de paroles
- Rappeler souvent les termes techniques
- Faire plus de pause
- Montrer précisement l'emplecement des fonctionnalités à l'écran
-->

---
layout: two-cols
name: feat | Dictionnaire
clicks: 2
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Dictionnaire</AbsoluteTitle>

<div class="mt-25" />

- Améliorations vs Excel
    - Une information plus accessible
    - Des exemples pour guider l'utilisateur

<hr class="my-5 mr-4">

- Informations sur un fichier attendu
- Exemple à faire <mdi-check class="text-green-400 inline" />
- Exemple à ne pas faire <mdi-close class="text-red-400 inline" />
- Écris par les documentalistes
- Liste complète des fichiers disponible en consultation libre

::right::

<ZoomableImage src="/app/fonctionnalite-dictionnaire-ouvert.png" :zoomed-x="-220" :zoomed-y="-25" :scale="2.2" class="mt-38 rounded shadow" />

<Pagination />

<!--
Pour qu'un utilisateur comprenne la nature d'un document donnée, un dictionnaire est fourni qui permet de décrire l'attendu documentaire.

Des exemple conforme et non conforme sont également fournis afin de montrer les cas de refus usuels.
-->

---
layout: two-cols
name: feat | Suivi des DOE
clicks: 2
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Suivi des DOE</AbsoluteTitle>

<div class="mt-25" />

- Améliorations vs Excel
    - Un monitoring des tâches
    - Amélioration de la fiabilité : suppression de la boîte mail

<hr class="my-5 mr-4">

- Liste de tous les DOE
- Filtres
    - Chef de Projet
    - Etat DOE
    - Prochaine action / Dernière action
    - Type d'opération
    - Mot clé
    - Date de dernière action
- Bouton d'accès au DOE

::right::

<ZoomableImage src="/app/fonctionnalite-suivi-en-cours.png" :zoomed-x="-220" :zoomed-y="-5" :scale="2.2" class="mt-40 rounded shadow" />

<Pagination />

<!--
Tous les DOE sont répertoriés dans des suivis, qui permet de rapidement voir tous les DOE en attente de fourniture ou terminés.

A l'aide de filtre, on peut accéder directement a un DOE qui nous interesse.
-->

---
layout: two-cols
name: feat | DOE attendus
clicks: 2
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : DOE attendus</AbsoluteTitle>

<div class="mt-25" />

- Une nouvelle fonctionnalité qui permet de voir et de sélectionner les DOE en attente de fourniture

<hr class="my-5 mr-4">

- Filtres
    - Aménageurs
    - Type d'opé
    - Chef de Projet
    - Date FN6
    - Mot clé
- Sites ignorés
- Accès à la création du DOE prérempli

::right::

<ZoomableImage src="/app/fonctionnalite-doe-attendus.png" :zoomed-x="-230" :zoomed-y="-20" :scale="1.7" class="ml-5 mt-25 rounded shadow" />

<Pagination />

<!--
Un autre suivi permet d'afficher tous les DOE à fournir pour une entité donné. Si un DOE est commencé à partir de cette page, une partie du formulaire de création du DOE est remplis automatiquement à partir des informations du SI Orange.

Un administrateur peut également choisir d'ignorer un DOE
-->

---
layout: two-cols
name: feat | EDLE/EDLS manquants
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : EDLE/EDLS manquants</AbsoluteTitle>

<div class="mt-23" />

- Une nouvelle fonctionnalité : Simplifier l'utilisation en séparant les fournitures ultérieures

<hr class="my-5 mr-4">

- Fichiers fournis 6 mois après le DOE
- Fourniture en dehors du DOE
- Une fois fournis, le document est injecté automatiquement dans le DOE
- Filtres
    - Type de fichier (EDLE / EDLS)
    - Type d'opération
    - Dernière action
    - Date dernière action
    - Mots clés

::right::

<img src="/app/fonctionnalite-edle-edls-manquant.png" class="mt-40 rounded shadow" />

<Pagination />

<!--
Une fonctionnalité spécifique est la fourniture des EDLE/EDLS (Etat des lieux entrants / sortants).

Lorsque qu'orange est en cohabitation avec un autre opérateur, comme par exemple free, un état des lieux doit être fournis. Ces fichiers sont généralement fournis 6 mois après la cloture d'un DOE.

Afin d'éviter de surcharger le suivi des DOE qui sont en attente pendant 6 mois. La fourniture de ces fichiers ce font sur une autre page.

Une fois ce fichier fournis, il est automatiquement injecté dans le DOE.

Commentaires :
- Slide par compréhensible
- BENEFICE : Fluidifier la création du DOE, raccourcir les délais, génére moins de dysfonctionnement et de frustration pour les utilisateurs
-->

---
layout: two-cols
name: feat | Publication trame
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Modification et publication de la trame</AbsoluteTitle>

<div class="mt-30" />

- Améliorations vs Excel
    - Publication instantanée
    - Versionning pour vérifier la validité dans le temps

<hr class="my-5 mr-4">

- Liste des règles permettant de générer les fichiers attendus en fonction de la nature de l'opération
- Modification / Publication / Versionning de la trame
- Changements pas appliqués indirectement

::right::

<img src="/app/fonctionnalite-trame.png" class="ml-5 mt-25 rounded shadow" />

<Pagination />

<!--
La liste des fichiers attendus générer à la création d'un DOE n'est pas fixe. Elle est générer en fonction d'une trame modifiable.

Un problème que j'ai rencontrer lors de la création de cette fonctionnalité en version WEB qui n'existait pas en version Excel, c'est que les DOE en cours se retrouvait désynchronisé de la trame. Pour répondre à cette problématique j'ai utiliser un système de versionning et de publication de trame.

Une fois la trame publié tous les DOE en cours sont réanalysés afin d'avoir tous les fichiers manquants affichés. Les DOE validés restent sur une ancienne version de la trame.

Commentaire :
- Challenge pas problème
- BENEFICE A CHAQUE FOIS (même sur la slide)
- Avantage souplesse
-->

---
layout: two-cols
name: feat | Utilisateurs
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Gestion des utilisateurs et des droits</AbsoluteTitle>

<div class="mt-30" />

- Une nouvelle fonctionnalité : création de profils et gestion des droits
- Amélioration vs Excel :
  - Sécurisation des droits

<hr class="my-5 mr-4">

- Gestion des profils utilisateurs
- Role (Droits d'accès)
- UPR (Régions accessibles)
- Profile Orange / Totem

::right::

<img src="/app/fonctionnalite-user.png" class="ml-5 mt-30 rounded shadow" />

<Pagination />

<!--
L'outil permet également de gérer les droit des utilisateurs par UPR et par role (RBAC).

Le projet towerco a également imposé une différence entre profile Orange et Totem.

Commentaire:
prôfiles mal écri
role accent
-->

---
layout: two-cols
name: feat | Autres
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Autres</AbsoluteTitle>

<div class="mt-24" />

- De nombreuses fonctionnalités ajoutées
- Application innovante

<hr class="my-5 mr-4">

- Interconnexion Totem
- Build to suit ATC
- Mise à jour automatique à partir des applications du SI d'Orange
- Ouverture de l'outil aux prestataires (Accès internet)
- Mail de relance automatique
- Tableau de bord (statistiques)
- Exports CSV
- Paramètres de l'outil

::right::

<img src="/app/fonctionnalite-parametres-de-l-outil.png" class="mt-45 h-30 mx-auto rounded shadow" />

<Pagination />

<!--
Il existe beaucoup d'autres fonctionnalités comme par exemple :
- L'interconnexion avec Totem
- Les dossiers Build to suit ATC
- La mise à jour automatique des applications du SI d'orange
- Les mail de relance automatique
- Les tableau de bords permettant d'afficher des statistiques
- Les exports CSV
- Ou encore les paramètres de l'outil
-->

---
layout: two-cols
name: Méthodogie
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Méthodologie du projet</AbsoluteTitle>

<div class="mt-25" />

- Méthode agile
  - Réunion rapide tous les matins pour faire part des problèmatiques
  - Déploiement régulier pour avoir des boucles de retours rapides
  - Gestion et priorisation des features / bugs (kanban)
- Un développement au plus près des utilisateurs
  - Réunions régulières avec les acteurs concernés
  - Idées de nouvelles fonctionnalités
  - Découverte de bugs
- Devops
  - Intégration continue
  - Déploiement continu
  - Versionning
  - Monitoring

::right::

<div class="h-full flex flex-column items-center justify-center mt-10">
  <img src="/schema-devops.png" class="h-50 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Pour la réalisation de cette outil, nous avons fonctionné en méthode agile avec :
- Des réunions tous les matins pour remonter les différentes problématiques
- Des déploiement fréquents pour avoir des boucles de retours rapides
- Une gestion des tâches et des priorisations en mode Kanban

Nous avons également organiser beaucoup de réunion avec les utilisateurs futurs de l'application. Ces réunions ont permis de comprendre des fonctionnalités manquantes et de découvrir d'éventuels bug.

Afin d'assurer un déploiement fréquent, nous avons utilisé l'intégration et le déploiement continue qui permet de déployer rapidement et automatiquement les nouvelles versions de l'application.

Commentaire: Open source
-->

---
layout: two-cols
name: Stack technique
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Stack technique</AbsoluteTitle>

<div class="mt-25" />

- Back : NodeJS
  - Typescript
  - Framework : Express
  - GraphQL API : Postgraphile
- Front : VueJS
  - Typescript
  - Framework : Nuxt
  - API de composition
  - Génération de code pour l'API
- Base de données : PostgreSQL
  - Migrations : Graphile Migrate

::right::

<div class="mt-25 mb-5" />

- Tâche asynchrone / CRON / offload (worker)
  - Typescript
  - Graphile worker
- Stockage des fichiers : S3 (OJS)
- Déploiement
  - IAAS (Infrastucture as a Service)
  - Docker swarm
  - Gitlab CI/CD

<div class="flex flex-row">
  <img class="h-20 rounded shadow mx-2" src="/docker.jpg">
  <img class="h-20 rounded shadow mx-2" src="/nuxt.png">
  <img class="h-20 rounded shadow mx-2 p-1" src="/postgresql.png">
  <img class="h-20 rounded shadow mx-2 p-1" src="/gitlab.png">
</div>

<Pagination />

<!--
L'application est divisé en trois parties le backend (coté serveur), le frontend (coté client) et une troisième partis que j'ai appelé tâche asynchrone / CRON. Cette dernière partis permet de décharger les des tâches du temps de traitement des requêtes. Par exemple si un utilisateur demande la suppression d'un document, le client n'a pas besoin d'attendre que le fichier soit supprimé pour continuer à travailler.

Je ne vais pas rentrer dans le détails de toutes les technologies utilisés. Ce qu'il faut retenir c'est que les choix techniques m'ont permis :
- D'avoir une applications très performante
- De pouvoir ajouter de nouvelles fonctionnalités très rapidement
- D'assurer la maintenabilité de l'application
- D'assurer une qualité de service (uptime)
- De déployer de nouvelles fonctionnalité rapidement
-->

---
layout: two-cols
name: Diagramme de BDD
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Diagramme de base de données</AbsoluteTitle>

<div class="mt-40" />

- Un outil très fiable se basant sur une base de donnée relationnelle
- Capacité à traiter des milliers de transactions en simultané

::right::

<div class="h-full pt-20 pb-5 ml-5">
  <img src="/app/diagramme-bdd-partial.png" class="h-full rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Commentaires :

Cette outil apporte une grande fiabilité que nous n'avions pas auparavant

C'était très motivant pour moi

Le slide de comprendre la complexité du travail
-->

---
layout: cover
name: Le projet towerco
background: /background-towerco.jfif
---

# Le projet Towerco
### Un nouveau challenge pour l'outil DOE

---
layout: two-cols
name: Towerco
---

<Header />

<AbsoluteTitle :level="1">Le projet Towerco</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Description du projet</AbsoluteTitle>

<div class="mt-35" />

- Recentrer Orange sur son coeur de métier
- Céder du patrimoine immobilier (sites et pylones) Orange à une filliale
- S'adapter à la concurrence SFR (Hivory) et Bouygues (Cellnex)

::right::

<div class="h-full flex flex-column items-center justify-center">
  <img src="/orange-enseigne.jpg" class="h-60 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Comme j'ai expliqué en introduction, le projet de l'outil DOE s'est développé en parallèle d'un autre gros projet à Orange : le projet towerco.

A l'instar de SFR et de Bouygues, Orange a choisi de séparer son activité déploiement de réseau pour séparer ses opex et ses capex. Cette opération

Afin de mener à bien cette sission, la loi impose une session de la documentation. Néanmoins, pas toute la documentation ne dois être transférée. Afin d'opérer ce filtres et ce contrôle légal, 2 documentaliste ont été engagés par UPR.

L'outil DOE version Excel convenant parfaitement à cette utilisation. Nous avons développer une API pour faciliter et accélerer ce processus de contrôle de l'entiereté de la documentation. Sans ca, il aurait fallu plusieurs années pour contrôler tous les documents

Commentaires :
Cession du parc immobilier (sur la slide)
Donner souvent des exemples
Je vous évite des détails

PLUS DE SLIDE LA DESSUS

Extension de DOE à d'autre cas d'usage
Dans un premier temps d'une transformation structurelle de l'entreprise. Gain de temps e de qualité. Ca a permis de s'adapter dans un temps record.
Dans un second temps le challenge l'adaptation
L'entreprise pas ils ont voulus

FOCALISER SUR LE BENEFICE
En x temps au lieu
Avec les risques d'erreurs
Augmenter le retour sur investissement
Eviter au personnes d'éviter des faire des heures de saisie
C'était stratégique pour l'entreprise
Le bénéfice
C'est très p
-->

---
layout: two-cols
name: Phase 1 | Cession des documents
---

<Header />

<AbsoluteTitle :level="1">Le projet Towerco</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Phase 1 : Cession des documents</AbsoluteTitle>

<div class="mt-30" />

- Transfert sécurisé de la documentation : L'Outil DOE est un outil idéal pour cet objectif
- Obligation légale de fournir une documentation
- 2 documentalistes par UPR
- 2.5 To de données à trier, filtrer et transférer
- Dépôt des documents sous S3
- **L'outil a économisé plusieurs dizaine de milliers d'€ à Orange**

::right::

<div class="h-full flex flex-column items-center justify-center">
  <img src="/antenne-totem.jpg" class="h-60 rounded shadow d-block mx-auto" />
</div>

<Pagination />

---
layout: two-cols
name: Phase 2 | Adaptation de l'outil
---

<Header />

<AbsoluteTitle :level="1">Le projet Towerco</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Phase 2 : Adaptation de l'outil</AbsoluteTitle>

<div class="mt-40" />

- Adaptation de l'outil pour anticiper les nouveaux processus d'Orange
- Ajout des profil Totem
- Trâme différente

::right::

<div class="h-full flex flex-column items-center justify-center">
  <img src="/totem-orange.webp" class="h-60 rounded shadow d-block mx-auto" />
</div>

<Pagination />

---
layout: two-cols
name: Résultats / Reflexions
---

<Header />

<AbsoluteTitle :level="1">Résultats & Pistes de réflexion</AbsoluteTitle>

<div class="mt-18" />

- Apprentissages
  - Complexité du SI d'Orange
  - Gestion de projet
  - Beaucoup de compétences techniques
  - Autonomie professionnel
- Résultats
  - Projet stratégique au niveau national <mdi-check class="inline text-green-400 animate-pulse" />
  - Application en production <mdi-check class="inline text-green-400 animate-pulse" />
  - Interfaces intuitives <mdi-check class="inline text-green-400 animate-pulse" />
  - Application performante <mdi-check class="inline text-green-400 animate-pulse" />
- Perspectives
  - L'application continue d'être maintenue
  - Embauche d'une régie pour assurer la pérénnisation du projet
  - Application mobile envisagée

::right::

<div class="h-full flex flex-column items-center justify-center ">
  <img src="/improvements.jpg" class="h-50 rounded shadow d-block mx-auto" />
</div>

<Pagination />

<!--
Au cours de ces trois années d'apprentissage j'ai énormément appris que ce soit au niveau technique que humain.

Ce PFE m'a permis de porter un projet de A à Z et d'être l'interlocuteur privilégié au niveau du national.

J'ai appris à surmonter beaucoup d'obstacle technique ou humain.

J'ai eu une expérience de la conduite de projet, j'ai passé beaucoup de temps réunions, des discussions qui sont relativement longues et fastidieuse et parfois sans résultats concrets.

Commentaire :


QUE DES PHRASES JE, J'ai acquis, j'ai su, j'ai améliorer
L'entreprise Orange dont le service informatique est complexe

Transformation stratégique.

A l'issu de ce projet une personne va être embaucher pour maintenir et développer le projet.

J'ai appris
-->

---
layout: default
name: Merci de votre écoute
---

<Header />

<AbsoluteTitle :level="1" top-class="top-60">Merci de votre écoute</AbsoluteTitle>

<Pagination />

<!--
Je vous remercie de votre écoute.
-->
