<template>
  <button
    @click="toggleTheme"
    :class="{
      'bg-blue-300 text-white': isDarkMode,
      'bg-yellow-300 text-gray-900': !isDarkMode,
    }"
    class="fixed rounded-full shadow-md"
  >
    <span class="sr-only">Toggle Dark Mode</span>
    <img
      v-if="isDarkMode"
      class="h-6 w-6"
      src="../assets/moon.png"
      viewBox="0 0 24 24"
    />
    <img v-else class="h-6 w-6" viewBox="0 0 24 24" src="../assets/sun.png" />
  </button>
</template>

<script>
export default {
  data() {
    return {
      isDarkMode: false,
    };
  },
  methods: {
    toggleTheme() {
      this.isDarkMode = !this.isDarkMode;
      const html = document.querySelector("html");
      html.classList.toggle("dark");
      console.log("dark");
    },
  },
};
</script>

<style scoped>
button {
  bottom: 20px;
  left: 20px;
  padding: 10px;
}
button:focus {
  outline: none;
}
</style>
