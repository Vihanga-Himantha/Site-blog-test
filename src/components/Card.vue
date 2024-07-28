<template>
  <q-card class="card">
    <q-img :src="image" :alt="title" />
    <q-card-section>
      <q-card-title>{{ title }}</q-card-title>
      <q-card-subtitle>{{ description }}</q-card-subtitle>
    </q-card-section>
    <q-card-actions align="right">
      <q-btn flat @click="viewMore">View More</q-btn>
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
  },
  methods: {
    viewMore() {
      this.$emit('view-more');
    },
  },
};
</script>

<style scoped>
.card {
  max-width: 400px;
  margin: 20px;
}
</style>
