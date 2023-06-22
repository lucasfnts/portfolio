<template>
  <div class="relative bg-indigo-700 dark:bg-slate-800 py-24 sm:py-32 lg:py-40">
    <div
      class="mx-auto max-w-md px-6 text-center sm:max-w-3xl lg:max-w-7xl lg:px-8"
    >
      <h2 class="text-lg font-semibold dark:text-indigo-400 text-black">
        SKILLS
      </h2>
      <p class="mt-2 text-3xl font-bold tracking-tight text-white sm:text-4xl">
        Voici l'ensemble de mes compétences
      </p>
      <p class="mx-auto mt-5 max-w-prose text-xl text-white">
        N'hésitez pas à me contacter pour évaluer vos besoins.
      </p>
      <div class="mt-20">
        <div class="grid grid-cols-1 gap-12 sm:grid-cols-2 lg:grid-cols-3">
          <div v-for="feature in features" :key="feature.name" class="pt-6">
            <div
              class="flow-root rounded-lg dark:bg-slate-400 bg-gray-50 px-6 pb-8"
            >
              <div class="-mt-6">
                <div>
                  <span
                    class="inline-flex items-center justify-center rounded-xl bg-indigo-500 dark:bg-slate-600 p-3 shadow-lg"
                  >
                    <component
                      :is="feature.icon"
                      class="h-8 w-8 text-white"
                      aria-hidden="true"
                    />
                  </span>
                </div>
                <h3
                  class="mt-8 text-lg font-semibold leading-8 tracking-tight text-gray-900"
                >
                  {{ feature.name }}
                </h3>
                <p class="mt-5 text-base leading-7 text-gray-600">
                  {{ feature.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import {
  ArrowPathIcon,
  CloudArrowUpIcon,
  CogIcon,
  LockClosedIcon,
  ServerIcon,
  ShieldCheckIcon,
} from "@heroicons/vue/24/outline";

const features = [
  {
    name: "Application Web",
    description:
      "Je réalise et héberge vos applications grace au framework Vue.js.",
    icon: CloudArrowUpIcon,
  },
  {
    name: "Back-End",
    description: "Création d'API sur-mesure, DevOps (Docker, CD/CI). ",
    icon: CogIcon,
  },
  {
    name: "Gestion de nom de Domaine",
    description:
      "Certificats SSL, gestions d'e-mails au nom de votre entreprise.",
    icon: LockClosedIcon,
  },
  {
    name: "RGPD",
    description: "Audit & mise en conformité RGPD pour les PME, DPO externe.",
    icon: ShieldCheckIcon,
  },
  {
    name: "Sauvegardes Sécurisées",
    description:
      "Configuration de sauvegarde automatiques et sécurisées pour vos données sensibles: vers un NAS, Cloud Privé ou Public.",
    icon: ServerIcon,
  },
  {
    name: "Souveraineté Numérique",
    description:
      "Je vous accompagne dans la mise en place de services auto-hébergé et respectueux de la vie privée.",
    icon: ArrowPathIcon,
  },
];
</script>
