<script setup>
import Hero from "./components/Hero.vue";
import Erp from "./components/Erp.vue";
import Divider from "./components/Divider.vue";
import Ecommerce from "./components/Ecommerce.vue";
import Skills from "./components/Skills.vue";
</script>

<template>
  <div>
    <Hero></Hero>
  </div>
  <div id="erp"><Erp></Erp></div>
  <Divider></Divider>
  <Ecommerce></Ecommerce>
  <Skills id="skills"></Skills>
</template>
