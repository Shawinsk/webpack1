<template>
  <q-layout view="lHh Lpr lFf" class="bg-dark text-white">
    <q-header class="bg-transparent text-white q-py-sm" style="backdrop-filter: blur(10px)">
      <q-toolbar>
        <q-toolbar-title class="text-weight-bold text-h5">
          <span class="text-primary">CRM</span> System
        </q-toolbar-title>

        <q-space />

        <div class="q-gutter-md gt-sm">
          <q-btn flat label="Home" color="white" />
          <q-btn flat label="Features" color="white" />
          <q-btn flat label="Pricing" color="white" />
          <q-btn flat label="Contact" color="white" />
        </div>

        <q-space />

        <div>
          <q-btn outline label="Log In" color="white" class="q-mr-sm" />
          <q-btn unelevated label="Get Started" color="primary" text-color="white" />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="bg-black text-white q-py-lg">
      <div class="text-center">
        <div class="text-h6 q-mb-md"><span class="text-primary">CRM</span> System</div>
        <div class="text-grey-5 q-mb-md">
          Manage your customers efficiently and grow your business today.
        </div>
        <div>&copy; {{ new Date().getFullYear() }} All rights reserved.</div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script setup>
// No script needed for this simple layout for now
</script>
