<template>
  <div class="relative overflow-hidden bg-white dark:bg-slate-800 pt-16 pb-32">
    <div class="relative">
      <div
        class="lg:mx-auto lg:grid lg:max-w-7xl lg:grid-flow-col-dense lg:grid-cols-2 lg:gap-24 lg:px-8"
      >
        <div
          class="mx-auto max-w-xl px-6 lg:mx-0 lg:max-w-none lg:py-16 lg:px-0"
        >
          <div>
            <div class="mt-6 text-gray-500 dark:text-slate-400">
              <h2
                class="text-lg font-semibold text-indigo-700 dark:text-indigo-400"
              >
                Full-Stack
              </h2>

              <h2
                class="text-3xl font-bold tracking-tight text-gray-900 dark:text-slate-200"
              >
                E.R.P sur mesure
              </h2>
              <p class="mt-4 text-lg text-left dark:text-slate-400">
                J'ai mis en place un E.R.P pour un entreprise du secteur BTP
                afin de :
              </p>
              <ul class="list-disc text-left pl-4 dark:text-slate-400">
                <li>Gérer des comptes clients</li>
                <li>Créer des devis & factures</li>
                <li>Suivre des chantiers</li>
              </ul>
              <p class="mt-4 text-lg text-justify dark:text-slate-400">
                L'E.R.P est une Application Web lié à une base de données SQL
                via une API.
              </p>
              <h3
                class="text-xl font-bold tracking-tight text-gray-900 py-4 text-left dark:text-slate-200"
              >
                Fonctionnalités détaillées
              </h3>
              <ul class="list-disc text-left pl-4 dark:text-slate-400">
                <li>Authentification sécurisée</li>
                <li>Formulaires de suivi dynamiques</li>
                <li>Gestion de rôle</li>
                <li>Génération de PDF</li>
                <li>Liste avec tris</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="mt-12 sm:mt-16 lg:mt-0">
          <div
            class="-mr-48 pl-4 sm:pl-6 md:-mr-16 lg:relative lg:m-0 lg:h-full lg:px-0"
          >
            <img
              class="w-full rounded-xl shadow-xl ring-1 ring-black ring-opacity-5 lg:absolute lg:left-0 lg:h-full lg:w-auto lg:max-w-none"
              src="../assets/screen1.png"
              alt="Inbox user interface"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="mt-24">
      <div class="lg:mx-auto lg:max-w-7xl lg:gap-24 lg:px-4">
        <div
          class="mx-auto max-w-xl px-6 lg:col-start-2 lg:mx-0 lg:max-w-none lg:px-0"
        >
          <div>
            <div class="mt-6 dark:text-slate-400">
              <h3
                class="text-xl font-bold tracking-tight text-gray-900 dark:text-slate-200"
              >
                <em>Stack</em>
              </h3>
              <p class="mt-4 text-lg text-gray-500">
                <em> Application Web </em>: Quasar (Vue.js 2)
                <br />
                <em> API</em>: Serveur Express.js, Sequelize + PostgreSQL
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { SparklesIcon } from "@heroicons/vue/24/outline";
</script>
