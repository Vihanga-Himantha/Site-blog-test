<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <Toolbar />
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import Toolbar from 'components/Toolbar.vue';
defineOptions({
  name: 'MainLayout',
  components: {
    Toolbar
  }
})
</script>
