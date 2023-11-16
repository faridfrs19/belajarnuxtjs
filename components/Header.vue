<template>
  <header class="bg-blue-900 text-white py-6">
    <div class="container mx-auto flex justify-between items-center">
      <div>
        <NuxtLink to="/" class="text-3xl font-bold tracking-wider">SMKN 1 CIOMAS</NuxtLink>
      </div>
      <nav class="flex items-center space-x-6">
        <NuxtLink to="/" class="text-lg hover:text-gray-300 transition duration-300 ease-in-out">Home</NuxtLink>
        <NuxtLink to="/product" class="text-lg hover:text-gray-300 transition duration-300 ease-in-out">Products</NuxtLink>
        <NuxtLink to="/cart" class="text-lg hover:text-gray-300 transition duration-300 ease-in-out">Cart</NuxtLink>
      </nav>
    </div>
  </header>
</template>

<style scoped>
NuxtLink {
  transition: color 0.3s;
}

header {
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

header.scrolled {
  background-color: rgba(59, 130, 246, 1);
}

/* Style untuk judul navbar */
.text-3xl {
  font-family: 'Montserrat', sans-serif;
}

/* Style untuk tautan menu */
nav a {
  transition: color 0.3s;
}

/* Hover state untuk tautan menu */
nav a:hover {
  color: #f8f8f8;
}
</style>

<script>
export default {
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 50) {
        this.$el.classList.add("scrolled");
      } else {
        this.$el.classList.remove("scrolled");
      }
    }
  }
};
</script>
