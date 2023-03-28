<template>
  <div>
    <button v-if="showButton" @click="scrollToTop">Retour en haut</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showButton: false,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
    handleScroll() {
      this.showButton = window.pageYOffset > 300;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style scoped>
button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px;
  background-color: #646cff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: opacity 0.3s ease-in-out;
}

button:hover {
  opacity: 0.8;
}
</style>
