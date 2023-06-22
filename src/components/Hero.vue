<template>
  <div class="bg-gray-100 dark:bg-slate-800">
    <div class="px-6 pt-6 lg:px-8">
      <div>
        <nav class="flex h-9 items-center justify-between" aria-label="Global">
          <div class="flex lg:min-w-0 lg:flex-1" aria-label="Global">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Lucas FUENTES</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-8"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M2.25 15a4.5 4.5 0 004.5 4.5H18a3.75 3.75 0 001.332-7.257 3 3 0 00-3.758-3.848 5.25 5.25 0 00-10.233 2.33A4.502 4.502 0 002.25 15z"
                />
              </svg>
            </a>
          </div>
          <div class="flex lg:hidden">
            <button
              type="button"
              class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
              @click="mobileMenuOpen = true"
            >
              <span class="sr-only">Ouvrez le menu</span>
              <Bars3Icon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div
            class="hidden lg:flex lg:min-w-0 lg:flex-1 lg:justify-center lg:gap-x-12"
          >
            <a
              v-for="item in navigation"
              :key="item.name"
              :href="item.href"
              class="font-semibold text-gray-900 dark:text-indigo-400 hover:text-gray-900"
              >{{ item.name }}</a
            >
          </div>
        </nav>
        <Dialog as="div" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
          <DialogPanel
            focus="true"
            class="fixed inset-0 z-10 overflow-y-auto bg-white px-6 py-6 lg:hidden"
          >
            <div class="flex h-9 items-center justify-between">
              <div class="flex">
                <a href="#" class="-m-1.5 p-1.5">
                  <span class="sr-only">Lucas FUENTES</span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="h-8"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M2.25 15a4.5 4.5 0 004.5 4.5H18a3.75 3.75 0 001.332-7.257 3 3 0 00-3.758-3.848 5.25 5.25 0 00-10.233 2.33A4.502 4.502 0 002.25 15z"
                    />
                  </svg>
                </a>
              </div>
              <div class="flex">
                <button
                  type="button"
                  class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
                  @click="mobileMenuOpen = false"
                >
                  <span class="sr-only">Close menu</span>
                  <XMarkIcon class="h-6 w-6" aria-hidden="true" />
                </button>
              </div>
            </div>
            <div class="mt-6 flow-root">
              <div class="-my-6 divide-y divide-gray-500/10">
                <div class="space-y-2 py-6">
                  <a
                    v-for="item in navigation"
                    :key="item.name"
                    :href="item.href"
                    class="-mx-3 block rounded-lg py-2 px-3 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-400/10"
                  >
                    {{ item.name }}
                  </a>
                </div>
              </div>
            </div>
          </DialogPanel>
        </Dialog>
      </div>
    </div>
    <main>
      <div class="relative px-6 lg:px-8">
        <div class="mx-auto max-w-3xl pt-20 pb-32 sm:pt-48 sm:pb-40">
          <div>
            <div>
              <h1
                class="text-4xl font-bold tracking-tight sm:text-center sm:text-6xl dark:text-slate-200"
              >
                Ingénieur Software
              </h1>
              <p
                class="mt-6 text-lg leading-8 text-gray-600 sm:text-justify dark:text-slate-400"
              >
                Basé au Havre, je suis un Ingénieur Full Stack et Cloud fort
                d'expérience dans différentes industries. <br />Que vous ayez
                besoin d'une <strong>API</strong> pour un service interne, un
                <strong>E.R.P sur mesure</strong> ou un accompagnement vers la
                <strong>souveraineté numérique</strong> de votre entreprise je
                saurais vous guider vers la meilleure solution.
                <br />
                En tant que <strong>D.P.O</strong> (Data Protection Officer ou
                Délégué à la Protection des Données) je peux vous accompagner
                dans votre projet de mise en conformité RGPD. <br />Je
                privilégie les solutions <strong>Open-Source</strong> et
                <strong>respectueuse de la vie privée</strong>.
              </p>
              <div class="mt-8 flex gap-x-4 sm:justify-center">
                <a
                  href="#erp"
                  class="inline-block rounded-lg bg-indigo-600 dark:bg-indigo-800 px-4 py-1.5 text-base font-semibold leading-7 text-white shadow-sm ring-1 ring-indigo-600 dark:ring-indigo-800 dark:hover:ring-slate-400 hover:bg-indigo-700 hover:ring-indigo-700"
                >
                  Mes réalisations
                  <span class="text-indigo-200" aria-hidden="true">&rarr;</span>
                </a>
                <a
                  href="#skills"
                  class="inline-block rounded-lg px-4 py-1.5 text-base font-semibold leading-7 text-gray-900 ring-1 dark:ring-indigo-800 dark:hover:ring-slate-400 dark:text-white ring-gray-900/10 hover:ring-gray-900/20"
                >
                  Mes Compétences
                  <span class="text-gray-400" aria-hidden="true">&rarr;</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Dialog, DialogPanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";

const navigation = [
  { name: "Projects", href: "#erp" },
  { name: "Skills", href: "#skills" },
];

const mobileMenuOpen = ref(false);
</script>
