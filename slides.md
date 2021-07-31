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

# Sommaire

- Orange
- Contexte
  - Outil DOE version Excel
  - Projet Towerco
- Outil DOE Web
  - Pourquoi une version Web ?
  - Méthodologie du projet
  - Présentation technique
- Résultats et pistes d'amélioration
- Synthèse du PFE

<template v-slot:right>

<div class="h-full flex flex-column items-center justify-center">
  <img src="/antenne-orange-2.jpg" class="h-80 rounded shadow d-block mx-auto" />
</div>

</template>

<Pagination />

