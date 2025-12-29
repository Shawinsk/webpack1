<template>
  <q-page
    class="bg-dark text-white flex flex-center"
    style="
      background-image: radial-gradient(
        circle at 50% 10%,
        rgba(213, 0, 0, 0.1) 0%,
        rgba(0, 0, 0, 0) 50%
      );
    "
  >
    <div class="column items-center q-pa-lg" style="width: 100%; max-width: 450px">
      <div class="q-mb-xl text-center">
        <h1 class="text-h3 text-weight-bold q-mb-sm">
          <span class="text-primary">CRM</span> System
        </h1>
        <div class="text-grey-4">Welcome back! Please login to your account.</div>
      </div>

      <q-card
        class="text-white full-width q-pa-md no-shadow"
        style="border: 1px solid #333; border-radius: 16px; background-color: #121212"
      >
        <q-card-section>
          <q-form class="q-gutter-md">
            <q-input
              dark
              outlined
              v-model="email"
              label="Email Address"
              type="email"
              color="primary"
            >
              <template v-slot:prepend>
                <q-icon name="email" />
              </template>
            </q-input>

            <q-input
              dark
              outlined
              v-model="password"
              label="Password"
              type="password"
              color="primary"
            >
              <template v-slot:prepend>
                <q-icon name="lock" />
              </template>
            </q-input>

            <div class="row justify-between items-center text-caption">
              <q-checkbox dark v-model="remember" label="Remember me" color="primary" size="sm" />
              <a href="#" class="text-primary" style="text-decoration: none">Forgot Password?</a>
            </div>

            <q-btn unelevated color="primary" label="Log In" size="lg" class="full-width q-mt-md" />

            <div class="text-center q-mt-md text-grey-5">
              Don't have an account?
              <router-link to="/signup" class="text-primary" style="text-decoration: none"
                >Sign Up</router-link
              >
            </div>
          </q-form>
        </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const remember = ref(false)
</script>
