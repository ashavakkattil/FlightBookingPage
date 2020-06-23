<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated style="background: transparent">
      <q-toolbar style="color:grey">
        <q-toolbar-title>Flight Booking</q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",

  components: {},

  data() {
    return {};
  }
};
</script>
