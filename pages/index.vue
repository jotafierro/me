<template>
  <div
    class="container flex-col sm:flex-col md:flex-col lg:flex-row xl:flex-row"
  >
    <div class="p-20 text-justify">
      <p>👋 Bienvenido, mi nombre es</p>
      <h1 class="font-bold text-5xl">Jonathan Fierro</h1>
      <h2 class="text-4xl">Desarrollador de software 👨🏻‍💻</h2>
      <p class="mt-5">
        Disfruto creando sistemas informáticos, sitios web y recientemente
        aplicaciones móviles. Estos son algunos de los puntos que considero
        esenciales:
      </p>
      <ul class="list-disc ml-10 mt-2">
        <li>🚀 experiencias de alto rendimiento</li>
        <li>🤩 la simplicidad e innovación</li>
        <li>🧐 las buenas practicas</li>
        <li>🤔 los desafíos de ingenio 🤯 🤪</li>
      </ul>

      <p class="mt-5">
        Actualmente soy parte del equipo de ingeniería de
        <a
          href="https://www.u-planner.com"
          class="text-blue-600"
          target="_blank"
          rel="U-Planner"
          >U-Planner </a
        >, donde trabajo en una amplia variedad de proyectos interesantes y
        significativos a diario.
      </p>
      <p class="mt-5">
        puedo utilizar diferentes herramientas🛠 para generar soluciones que
        hagan la vida mas sencilla 🏖 .
      </p>
      <p class="mt-5">
        Aparte de programar. Soy esposo y padre de 2 hermosas pequeñas que me
        roban el ❤️ 👨‍👩‍👧‍👧, las cuales son la fuerza que me impulsan día a día 🏅.
      </p>
    </div>
    <div class="px-20 lg:pl-20 lg:px-0">
      <p class="mt-5">
        Algunas cosas con las cuales he trabajado que quiero destacar:
      </p>
      <ul class="list-disc mt-2 ml-10">
        <li>
          <p>Tecnologías/utilidades</p>
          <p class="mt-2">
            <a
              v-for="(tech, key) in iHaveWorkedWith.technologies"
              :key="key"
              href="#"
              class="inline-block"
            >
              <img :src="tech" :alt="key" class="pr-1" />
            </a>
          </p>
        </li>
        <li>
          <p>Lenguajes de programación</p>
          <p class="mt-2">
            <a
              v-for="(tech, key) in iHaveWorkedWith.languages"
              :key="key"
              href="#"
              class="inline-block"
            >
              <img :src="tech" :alt="key" class="pr-1" />
            </a>
          </p>
        </li>
        <li>
          <p>Bases de datos</p>
          <p class="mt-2">
            <a
              v-for="(tech, key) in iHaveWorkedWith.databases"
              :key="key"
              href="#"
              class="inline-block"
            >
              <img :src="tech" :alt="key" class="pr-1" />
            </a>
          </p>
        </li>
        <li>
          <p>Frameworks</p>
          <p class="mt-2">
            <a
              v-for="(tech, key) in iHaveWorkedWith.frameworks"
              :key="key"
              href="#"
              class="inline-block"
            >
              <img :src="tech" :alt="key" class="pr-1" />
            </a>
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
const iHaveWorkedWith = {
  technologies: {
    Git: 'https://img.shields.io/badge/-Git-F05032?logo=git&logoColor=fff',
    VSCode:
      'https://img.shields.io/badge/-VSCode-007ACC?logo=visual-studio-code&logoColor=fff',
    GitHub:
      'https://img.shields.io/badge/-GitHub-181717?logo=github&logoColor=fff',
    Bitbucket:
      'https://img.shields.io/badge/-Bitbucket-0052CC?logo=bitbucket&logoColor=fff',
    Jira: 'https://img.shields.io/badge/-Jira-0052CC?logo=jira&logoColor=fff',
    Trello:
      'https://img.shields.io/badge/-Trello-0079BF?logo=Trello&logoColor=fff',
    Azure:
      'https://img.shields.io/badge/-Azure-0089D6?logo=microsoft-azure&logoColor=fff',
    AWS:
      'https://img.shields.io/badge/-AWS-232F3E?logo=amazon-aws&logoColor=fff',
    Firebase:
      'https://img.shields.io/badge/-Firebase-FFCA22?logo=firebase&logoColor=fff',
    Heroku:
      'https://img.shields.io/badge/-Heroku-430098?logo=heroku&logoColor=fff',
    Slack:
      'https://img.shields.io/badge/-Slack-4A154B?logo=Slack&logoColor=fff',
    Teams:
      'https://img.shields.io/badge/-Teams-6264A7?logo=microsoft-teams&logoColor=fff',
    Sentry:
      'https://img.shields.io/badge/-Sentry-FB4226?logo=sentry&logoColor=fff',
    CircleCi:
      'https://img.shields.io/badge/-CircleCi-343434?logo=CircleCi&logoColor=fff',
  },
  languages: {
    Javascript:
      'https://img.shields.io/badge/-Javascript-F7DF1E?logo=Javascript&logoColor=fff',
    Python:
      'https://img.shields.io/badge/-Python-3776AB?logo=Python&logoColor=fff',
    Dart: 'https://img.shields.io/badge/-Dart-0175C2?logo=Dart&logoColor=fff',
    Golang: 'https://img.shields.io/badge/-Golang-00ADD8?logo=go&logoColor=fff',
    Typescript:
      'https://img.shields.io/badge/-Typescript-007ACC?logo=Typescript&logoColor=fff',
    PHP: 'https://img.shields.io/badge/-PHP-777BB4?logo=PHP&logoColor=fff',
  },
  databases: {
    MongoDB:
      'https://img.shields.io/badge/-MongoDB-47A248?logo=MongoDB&logoColor=fff',
    PostgreSQL:
      'https://img.shields.io/badge/-PostgreSQL-336791?logo=PostgreSQL&logoColor=fff',
    SQLite:
      'https://img.shields.io/badge/-SQLite-003B57?logo=SQLite&logoColor=fff',
    MariaDB:
      'https://img.shields.io/badge/-MariaDB-003545?logo=MariaDB&logoColor=fff',
  },
  frameworks: {
    ' Node.js':
      'https://img.shields.io/badge/-Node.js-339933?logo=Node.js&logoColor=fff',
    'Vue.js':
      'https://img.shields.io/badge/-Vue.js-4FC08D?logo=vue.js&logoColor=fff',
    'Nuxt.js':
      'https://img.shields.io/badge/-Nuxt.js-00C58E?logo=Nuxt.js&logoColor=fff',
    Flutter:
      'https://img.shields.io/badge/-Flutter-02569B?logo=flutter&logoColor=fff',
    Laravel:
      'https://img.shields.io/badge/-Laravel-FF2D20?logo=Laravel&logoColor=fff',
    Bootstrap:
      'https://img.shields.io/badge/-Bootstrap-563D7C?logo=Bootstrap&logoColor=fff',
    TailwindCss:
      'https://img.shields.io/badge/-Tailwind_css-563D7C?logo=Tailwind-Css&logoColor=fff',
  },
}

export default {
  data() {
    return {
      iHaveWorkedWith,
    }
  },
}
</script>

<style>
html {
  background-color: #fff;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 304 304' width='304' height='304'%3E%3Cpath fill='%23e3e3e3' fill-opacity='0.23' d='M44.1 224a5 5 0 1 1 0 2H0v-2h44.1zm160 48a5 5 0 1 1 0 2H82v-2h122.1zm57.8-46a5 5 0 1 1 0-2H304v2h-42.1zm0 16a5 5 0 1 1 0-2H304v2h-42.1zm6.2-114a5 5 0 1 1 0 2h-86.2a5 5 0 1 1 0-2h86.2zm-256-48a5 5 0 1 1 0 2H0v-2h12.1zm185.8 34a5 5 0 1 1 0-2h86.2a5 5 0 1 1 0 2h-86.2zM258 12.1a5 5 0 1 1-2 0V0h2v12.1zm-64 208a5 5 0 1 1-2 0v-54.2a5 5 0 1 1 2 0v54.2zm48-198.2V80h62v2h-64V21.9a5 5 0 1 1 2 0zm16 16V64h46v2h-48V37.9a5 5 0 1 1 2 0zm-128 96V208h16v12.1a5 5 0 1 1-2 0V210h-16v-76.1a5 5 0 1 1 2 0zm-5.9-21.9a5 5 0 1 1 0 2H114v48H85.9a5 5 0 1 1 0-2H112v-48h12.1zm-6.2 130a5 5 0 1 1 0-2H176v-74.1a5 5 0 1 1 2 0V242h-60.1zm-16-64a5 5 0 1 1 0-2H114v48h10.1a5 5 0 1 1 0 2H112v-48h-10.1zM66 284.1a5 5 0 1 1-2 0V274H50v30h-2v-32h18v12.1zM236.1 176a5 5 0 1 1 0 2H226v94h48v32h-2v-30h-48v-98h12.1zm25.8-30a5 5 0 1 1 0-2H274v44.1a5 5 0 1 1-2 0V146h-10.1zm-64 96a5 5 0 1 1 0-2H208v-80h16v-14h-42.1a5 5 0 1 1 0-2H226v18h-16v80h-12.1zm86.2-210a5 5 0 1 1 0 2H272V0h2v32h10.1zM98 101.9V146H53.9a5 5 0 1 1 0-2H96v-42.1a5 5 0 1 1 2 0zM53.9 34a5 5 0 1 1 0-2H80V0h2v34H53.9zm60.1 3.9V66H82v64H69.9a5 5 0 1 1 0-2H80V64h32V37.9a5 5 0 1 1 2 0zM101.9 82a5 5 0 1 1 0-2H128V37.9a5 5 0 1 1 2 0V82h-28.1zm16-64a5 5 0 1 1 0-2H146v44.1a5 5 0 1 1-2 0V18h-26.1zm102.2 270a5 5 0 1 1 0 2H98v14h-2v-16h124.1zM242 149.9V160h16v34h-16v62h48v48h-2v-46h-48v-66h16v-30h-16v-12.1a5 5 0 1 1 2 0zM53.9 18a5 5 0 1 1 0-2H64V2H48V0h18v18H53.9zm112 32a5 5 0 1 1 0-2H192V0h50v2h-48v48h-28.1zm-48-48a5 5 0 0 1-9.8-2h2.07a3 3 0 1 0 5.66 0H178v34h-18V21.9a5 5 0 1 1 2 0V32h14V2h-58.1zm0 96a5 5 0 1 1 0-2H137l32-32h39V21.9a5 5 0 1 1 2 0V66h-40.17l-32 32H117.9zm28.1 90.1a5 5 0 1 1-2 0v-76.51L175.59 80H224V21.9a5 5 0 1 1 2 0V82h-49.59L146 112.41v75.69zm16 32a5 5 0 1 1-2 0v-99.51L184.59 96H300.1a5 5 0 0 1 3.9-3.9v2.07a3 3 0 0 0 0 5.66v2.07a5 5 0 0 1-3.9-3.9H185.41L162 121.41v98.69zm-144-64a5 5 0 1 1-2 0v-3.51l48-48V48h32V0h2v50H66v55.41l-48 48v2.69zM50 53.9v43.51l-48 48V208h26.1a5 5 0 1 1 0 2H0v-65.41l48-48V53.9a5 5 0 1 1 2 0zm-16 16V89.41l-34 34v-2.82l32-32V69.9a5 5 0 1 1 2 0zM12.1 32a5 5 0 1 1 0 2H9.41L0 43.41V40.6L8.59 32h3.51zm265.8 18a5 5 0 1 1 0-2h18.69l7.41-7.41v2.82L297.41 50H277.9zm-16 160a5 5 0 1 1 0-2H288v-71.41l16-16v2.82l-14 14V210h-28.1zm-208 32a5 5 0 1 1 0-2H64v-22.59L40.59 194H21.9a5 5 0 1 1 0-2H41.41L66 216.59V242H53.9zm150.2 14a5 5 0 1 1 0 2H96v-56.6L56.6 162H37.9a5 5 0 1 1 0-2h19.5L98 200.6V256h106.1zm-150.2 2a5 5 0 1 1 0-2H80v-46.59L48.59 178H21.9a5 5 0 1 1 0-2H49.41L82 208.59V258H53.9zM34 39.8v1.61L9.41 66H0v-2h8.59L32 40.59V0h2v39.8zM2 300.1a5 5 0 0 1 3.9 3.9H3.83A3 3 0 0 0 0 302.17V256h18v48h-2v-46H2v42.1zM34 241v63h-2v-62H0v-2h34v1zM17 18H0v-2h16V0h2v18h-1zm273-2h14v2h-16V0h2v16zm-32 273v15h-2v-14h-14v14h-2v-16h18v1zM0 92.1A5.02 5.02 0 0 1 6 97a5 5 0 0 1-6 4.9v-2.07a3 3 0 1 0 0-5.66V92.1zM80 272h2v32h-2v-32zm37.9 32h-2.07a3 3 0 0 0-5.66 0h-2.07a5 5 0 0 1 9.8 0zM5.9 0A5.02 5.02 0 0 1 0 5.9V3.83A3 3 0 0 0 3.83 0H5.9zm294.2 0h2.07A3 3 0 0 0 304 3.83V5.9a5 5 0 0 1-3.9-5.9zm3.9 300.1v2.07a3 3 0 0 0-1.83 1.83h-2.07a5 5 0 0 1 3.9-3.9zM97 100a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-48 32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32 48a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16-64a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 96a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-144a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-96 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm96 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16-64a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-32 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zM49 36a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-32 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zM33 68a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-48a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 240a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16-64a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm80-176a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32 48a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm112 176a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-16 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zM17 180a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0 16a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm0-32a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16 0a3 3 0 1 0 0-6 3 3 0 0 0 0 6zM17 84a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm32 64a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm16-16a3 3 0 1 0 0-6 3 3 0 0 0 0 6z'%3E%3C/path%3E%3C/svg%3E");
}

.container {
  @apply min-h-screen;
  @apply flex;
  @apply justify-start;
  @apply items-center;
  @apply font-sans;
}
</style>
