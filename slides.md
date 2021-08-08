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
5. Synthèse du PFE

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
  <li>
    Outil initialement développé sur Excel
    <ul>
      <li>Automatiser la documentation des travaux réalisé sur site</li>
      <li>Initialement 300+ documents fournis à chaque opération</li>
    </ul>
  </li>
  <li>Temps de traitement long</li>
  <li>Organisation du suivi complexe (boîte mail)</li>
  <li>Problématique de sécurité</li>
  <li>
    Certaines automatisations impossibles/compliqués
    <ul>
      <li>Connexion à BDE Site</li>
      <li>Push SFTP</li>
    </ul>
  </li>
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

<ul class="mt-25">
  <li>
    Simplifier l'expérience utilisateur
    <ul>
      <li>Interface utilisateur intuitive</li>
      <li>Limiter le nombre de clique pour contrôler les DOE</li>
      <li>Simplifier les processus</li>
      <li>Limiter un maximum le nombre d'outil nécessaire au contrôle d'un DOE</li>
    </ul>
  </li>
  <li>
    Répondre aux limitations de VBA
    <ul>
      <li>Archivage de toutes les données (S3)</li>
      <li>Interconnexion aux applications du SI Orange</li>
      <li>Augmenter la sécurisation des données (RGPD)</li>
    </ul>
  </li>
</ul>

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
</ul>

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/schema-devops.png" class="h-50 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

---
layout: two-cols
---
<Header />

<AbsoluteTitle :level="1">Outil DOE Web</AbsoluteTitle>
<AbsoluteTitle :level="3" top-class="top-20">Présentation technique</AbsoluteTitle>

<Pagination />
