<template>
  <q-toolbar class="bg-primary text-white shadow-2">
    <q-btn flat round dense icon="menu" class="q-mr-sm" />




    <q-separator dark vertical inset />
    <router-link to="/" class="router-link">
      <q-btn stretch flat label="Home" />
    </router-link>


    <q-space />


    <!--
    <q-btn-dropdown stretch flat label="Dropdown">
      <q-list>
        <q-item-label header>Folders</q-item-label>
        <q-item v-for="n in 3" :key="`x.${n}`" clickable v-close-popup tabindex="0">
          <q-item-section avatar>
            <q-avatar icon="folder" color="secondary" text-color="white" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Photos</q-item-label>
            <q-item-label caption>February 22, 2016</q-item-label>
          </q-item-section>
          <q-item-section side>
            <q-icon name="info" />
          </q-item-section>
        </q-item>
        <q-separator inset spaced />
        <q-item-label header>Files</q-item-label>
        <q-item v-for="n in 3" :key="`y.${n}`" clickable v-close-popup tabindex="0">
          <q-item-section avatar>
            <q-avatar icon="assignment" color="primary" text-color="white" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Vacation</q-item-label>
            <q-item-label caption>February 22, 2016</q-item-label>
          </q-item-section>
          <q-item-section side>
            <q-icon name="info" />
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown>

    -->



    <q-separator dark vertical />
    <router-link to="/blog" class="router-link">
      <q-btn stretch flat label="Blog" />
    </router-link>





    <q-separator dark vertical />
    <router-link to="/about" class="router-link">
      <q-btn stretch flat label="About" />
    </router-link>




  </q-toolbar>
</template>



<script>
export default {
  name: 'Toolbar',
};
</script>

<style scoped>
.q-toolbar {
  padding: 0 !important; /* Ensure no padding */
}


.router-link {
  text-decoration: none;
}


</style>
