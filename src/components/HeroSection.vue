<template>
  <div class="hero">
    <div class="hero-content">
      <h1>{{ title }}</h1>
      <p>{{ subtitle }}</p>
      <q-btn color="primary" @click="learnMore">Learn More</q-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
  methods: {
    learnMore() {
      this.$emit('learn-more');
    },
  },
};
</script>

<style scoped>
.hero {
  background-image: url("https://www.hubspot.com/hs-fs/hubfs/hero-image_5-1.webp?width=893&height=600&name=hero-image_5-1.webp");
  background-size: cover;
  background-position: center;
  height: 100vh; /* Full viewport height */
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  margin: 0; /* Remove margins */
  padding: 0; /* Remove paddings */
}

.hero-content {
  background-color: rgba(0, 0, 0, 0.5);
  padding: 20px;
  border-radius: 10px;
}

.hero-content h1 {
  font-size: 3em;
  margin: 0;
}

.hero-content p {
  font-size: 1.5em;
  margin: 10px 0;
}

.q-btn {
  margin-top: 20px;
}

@media (min-width: 600px) and (max-width: 1439.98px) {
  .hero {
    padding: 0 !important; /* Remove padding for specific media query */
  }
}
</style>

