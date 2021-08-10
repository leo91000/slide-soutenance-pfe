---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /antennes-orange.jpg
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Page de couverture soutenance
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

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Sommaire</AbsoluteTitle>

<div class="mt-22"></div>

1. Orange
2. Contexte
    - Outil DOE version Excel
    - Projet Towerco
3. Outil DOE Web
    - Pourquoi une version Web ?
    - Méthodologie du projet
    - Présentation de l'outil
    - Présentation technique
4. Résultats et pistes d'amélioration

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/antenne-orange-2.jpg" class="h-80 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: two-cols
---


<Header />

<AbsoluteTitle :level="1">Présentation de Orange</AbsoluteTitle>

<div class="mt-40"></div>

- Opérateur de Télécommnunications
- Solutions B2B & B2C
- Leader historique sur le marché
- 1<sup>er</sup> opérateur mobile pour la 10<sup>ème</sup> année consécutive selon l'Arcep

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/orange.png" class="h-80 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Présentation de mon département</AbsoluteTitle>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/upr-ne.png" class="h-80 d-block mx-auto" />
</div>


<template v-slot:right>

<div class="mt-25">
  <ul>
    <li>
      L'<span class="font-bold underline">Unité de Pilotage Réseau</span>
      <ul>
        <li>IRM (Ingénierie Réseau Mobile)</li>
        <li>OPR (Opération Performance Réseau mobile)</li>
        <li>APR (Anticipation Programmation Réseau Fixe)</li>
        <li>
          <span class="font-bold underline">DEP (Déploiement Réseau Mobile)</span>
          <ul>
            <li>Conception et Négoication Sites Mobiles</li>
            <li>Pilotage Production Mobile Nord Est</li>
            <li class="font-bold underline">Performances Relations Bailleurs</li>
            <li>...</li>
          </ul>
        </li>
        <li>...</li>
      </ul>
    </li>
  </ul>
</div>


</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Contexte de l'application</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Outil DOE Version Excel</AbsoluteTitle>

<div class="mt-25" />

<ul>
  <li>DOE = <span class="font-bold">D</span>ossier d'<span class="font-bold">O</span>uvrage <span class="font-bold">E</span>xécuté</li>
  <li>Initialement 300+ documents fournis à chaque opération</li>
  <li>
    Outil initialement développé sur Excel
  </li>
  <li>Automatiser la documentation des travaux réalisé sur site</li>
  <li>Entre 5 et 50 documents maximum avec l'outil</li>
  <li>Suivi des DOES traités par boîte mail</li>
</ul>

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/doe-excel-profil-ame.png" class="h-60 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />


---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Contexte de l'application</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Projet Towerco</AbsoluteTitle>

<div class="mt-25" />

<ul>
  <li>Session du parc d'antenne Orange à une filliale</li>
  <li>Faire concurrence à SFR (Hivory) et Bouygues (Cellnex)</li>
  <li>Obligation légale de fournir une documentation</li>
  <li>2 documentaliste par UPR</li>
  <li>2.5 To de données à trier, filtrer et transférer</li>
  <li>Réutilisation de l'outil Excel avec un serveur d'API</li>
  <li>Dépôt des documents sous S3</li>
</ul>

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/orange-enseigne.jpg" class="h-60 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Pourquoi une version WEB ?</AbsoluteTitle>

<ul class="mt-20">
  <li>
    Simplifier l'expérience utilisateur
    <ul>
      <li>Interface utilisateur intuitive</li>
      <li>Limiter le nombre de clique pour contrôler les DOE</li>
      <li>Simplifier les processus</li>
      <li>Limiter le nombre d'outil nécessaire au contrôle d'un DOE</li>
    </ul>
  </li>
  <li>
    Répondre aux limitations de VBA
    <ul>
      <li>Archivage de toutes les données (S3)</li>
      <li>Interconnexion aux applications du SI Orange</li>
      <li>Réduire les temps de traitement</li>
      <li>Décomplexifier le suivi (boîte mail en VBA)</li>
      <li>Problématique de sécurité</li>
      <li>
        Automatiser ce qui est impossibles/compliqués en VBA
        <ul>
          <li>Connexion à BDE Site</li>
          <li>Push SFTP</li>
        </ul>
      </li>
    </ul>
  </li>
  <li>Augmenter la sécurisation des données (RGPD)</li>
</ul>

<template v-slot:right>
  <div class="h-full flex flex-column items-center justify-center px-10">
    <img src="/web.jpg" class="w-full rounded shadow d-block mx-auto" />
  </div>
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Création du DOE</AbsoluteTitle>

<div class="mt-25" />

- Renseignement des informations sur l'opération
    - Code opération
    - Type d'opération
    - Bandes de fréquence
    - Recetteur
    - ...
- Génération des cases à cocher
    - Détails plus spécifiques
    - Généré en fonction du type d'opération

<template v-slot:right>
  <img src="/app/fonctionnalite-nouveau-suivi-doe.png" class="mt-25 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Dépôt/Contrôle des documents</AbsoluteTitle>

<div class="mt-25" />

- Fichier attendus générés automatiquement
- Obligatoire / Conditionelle
- Fichiers fournis assignés aux fichiers attendus correspondant
- Fichier OK ou NOK ou Fourniture ultérieur
- Outil de renommage automatique à une règle donné
- Visionneuse de documents
- Contrôle
    - Refuser
    - Valider
    - Valider avec complément
    - Valider sans contrôle


<template v-slot:right>
  <img src="/app/fonctionnalite-controle-des-documents.png" class="ml-5 mt-35 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Suivi des DOE</AbsoluteTitle>

<div class="mt-25" />

- Liste de tous les DOE
- Filtres
    - Chef de Projet
    - Etat DOE
    - Prochaine action / Dernière action
    - Type d'opération
    - Mot clé
    - Date de dernière action
- Bouton d'accès au DOE

<template v-slot:right>
  <img src="/app/fonctionnalite-suivi-en-cours.png" class="mt-40 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : DOE attendus</AbsoluteTitle>

<div class="mt-25" />

- Liste de DOE non fournis (import SI)
- Filtres
    - Amenageurs
    - Type d'opé
    - Chef de Projet
    - Date FN6
    - Mot clé
- Sites ignorés
- Accès à la création du DOE prérempli

<template v-slot:right>
  <img src="/app/fonctionnalite-doe-attendus.png" class="mt-25 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : EDLE/EDLS manquants</AbsoluteTitle>

<div class="mt-25" />

- Fichiers fournis 6 mois après le DOE
- Fourniture en dehors du DOE
- Une fois fournis, le document est injecté automatiquement dans le DOE
- Filtres
    - Type de fichier (EDLE / EDLS)
    - Type d'opération
    - Dernière action
    - Date dernière action
    - Mots clés

<template v-slot:right>
  <img src="/app/fonctionnalite-edle-edls-manquant.png" class="mt-40 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Dictionnaire</AbsoluteTitle>

<div class="mt-40" />

- Informations sur un fichier attendu
- Exemple à faire <mdi-check class="text-green-400 inline" />
- Exemple à ne pas faire <mdi-close class="text-red-400 inline" />
- Ecris par les documentaliste
- Liste complète des fichiers disponible en consultation libre

<template v-slot:right>
  <img src="/app/fonctionnalite-dictionnaire-ouvert.png" class="mt-38 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Modification et publication de la trame</AbsoluteTitle>

<div class="mt-40" />

- Liste des règles permettant de générer les fichiers attendus en fonction de la nature de l'opération
- Modification / Publication / Versionning de la trame
- Changements pas apliqués indirectement

<template v-slot:right>
  <img src="/app/fonctionnalite-trame.png" class="ml-5 mt-25 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Gestion des utilisateurs et des droits</AbsoluteTitle>

<div class="mt-40" />

- Gestion des profiles utilisateurs
- Role (Droits d'accès)
- UPR (Régions accessibles)
- Profile Orange / Totem

<template v-slot:right>
  <img src="/app/fonctionnalite-user.png" class="ml-5 mt-30 rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---

<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Fonctionnalités de l'application : Autres</AbsoluteTitle>

<ul class="mt-30">
  <li>
    Interconnexion Totem
  </li>
  <li>
    Build to suit ATC
  </li>
  <li>Mise à jour automatique à partir des applications du SI d'Orange</li>
  <li>Ouverture de l'outil aux prestataires (Accès internet)</li>
  <li>Mail de relance automatique</li>
  <li>Tableau de bord (statistiques)</li>
  <li>Exports CSV</li>
  <li>Paramètres de l'outil</li>
</ul>

<template v-slot:right>
  <img src="/app/fonctionnalite-parametres-de-l'outil.png" class="mt-45 h-30 mx-auto rounded shadow" />
</template>

<Pagination />

---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Méthodologie du projet</AbsoluteTitle>

<ul class="mt-25">
  <li>
    Méthode agile
    <ul>
      <li>Réunion répide tous les matins pour faire par des problèmatiques</li>
      <li>Déploiement régulier pour avoir des boucles de retour rapides</li>
      <li>Gestion et priorisation des features / bugs (kanban)</li>
    </ul>
  </li>
  <li>
    Réunion régulières avec les acteurs concernés
    <ul>
      <li>Idées de nouvelle fonctionnalités</li>
      <li>Découverte de bugs</li>
    </ul>
  </li>
  <li>
    Devops
    <ul>
      <li>Intégration continue</li>
      <li>Déploiement continue</li>
      <li>Versionning</li>
      <li>Monitoring</li>
    </ul>
  </li>
</ul>

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center mt-10">
  <img src="/schema-devops.png" class="h-50 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Stack technique</AbsoluteTitle>

<ul class="mt-25">
  <li>
    Back : NodeJS
    <ul>
      <li>Typescript</li>
      <li>Framework : Express</li>
      <li>GraphQL API : Postgraphile</li>
    </ul>
  </li>
  <li>
    Front : VueJS
    <ul>
      <li>Typescript</li>
      <li>Framework : Nuxt</li>
      <li>API de composition</li>
      <li>Génération de code pour l'API</li>
    </ul>
  </li>
  <li>
    Base de données : PostgreSQL
    <ul>
      <li>Migrations : Graphile Migrate</li>
    </ul>
  </li>
</ul>

<template v-slot:right>

<ul class="mt-25 mb-5">
  <li>
    Tâche asynchrone / CRON / offload (worker)
    <ul>
      <li>Typescript</li>
      <li>Graphile worker</li>
    </ul>
  </li>
  <li>
    Stockage des fichiers : S3 (OJS)
  </li>
  <li>
    Déploiement
    <ul>
      <li>IAAS (Infrastucture as a Service)</li>
      <li>Docker swarm</li>
      <li>Gitlab CI/CD</li>
    </ul>
  </li>
</ul>

<div class="flex flex-row">
  <img class="h-20 rounded shadow mx-2" src="/docker.jpg">
  <img class="h-20 rounded shadow mx-2" src="/nuxt.png">
  <img class="h-20 rounded shadow mx-2 p-1" src="/postgresql.png">
  <img class="h-20 rounded shadow mx-2 p-1" src="/gitlab.png">
</div>

</template>

<Pagination />

---
layout: default
---
<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Diagramme de base de données</AbsoluteTitle>

<div class="h-full pt-20 pb-5">
  <img src="/app/diagramme-bdd-partial.png" class="h-full rounded shadow d-block mx-auto" />
</div>

<Pagination />

---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Résultats et pistes d'amélioration</AbsoluteTitle>

<ul class="mt-20">
  <li>
    Apprentissages
    <ul>
      <li>Complexité du SI d'Orange</li>
      <li>Politique interne</li>
    </ul>
  </li>
  <li>
    Pistes d'amélioration
    <ul>
      <li>Test unitaires</li>
      <li>Meilleur séparation du code (par domaine)</li>
      <li>Meilleur anticipation des besoins</li>
    </ul>
  </li>
  <li>
    Résultats
    <ul>
      <li>Application en production <mdi-check class="inline text-green-400 animate-pulse" /></li>
      <li>Interface intuitives <mdi-check class="inline text-green-400 animate-pulse" /></li>
      <li>Application performante <mdi-check class="inline text-green-400 animate-pulse" /></li>
    </ul>
  </li>
</ul>

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center ">
  <img src="/improvements.jpg" class="h-50 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: default
---
<Header />

<AbsoluteTitle :level="1" top-class="top-60">Merci de votre écoute</AbsoluteTitle>

<Pagination />



