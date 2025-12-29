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
        <div class="text-grey-4">Create your free account to get started.</div>
      </div>

      <q-card
        class="text-white full-width q-pa-md no-shadow"
        style="border: 1px solid #333; border-radius: 16px; background-color: #121212"
      >
        <q-card-section>
          <q-form class="q-gutter-md">
            <q-input dark outlined v-model="name" label="Full Name" color="primary">
              <template v-slot:prepend>
                <q-icon name="person" />
              </template>
            </q-input>

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

            <q-input
              dark
              outlined
              v-model="confirmPassword"
              label="Confirm Password"
              type="password"
              color="primary"
            >
              <template v-slot:prepend>
                <q-icon name="lock_clock" />
              </template>
            </q-input>

            <div class="row items-center text-caption">
              <q-checkbox dark v-model="agree" color="primary" size="sm" />
              <div class="q-ml-sm">
                I agree to the
                <a href="#" class="text-primary" style="text-decoration: none">Terms of Service</a>
                and
                <a href="#" class="text-primary" style="text-decoration: none">Privacy Policy</a>
              </div>
            </div>

            <q-btn
              unelevated
              color="primary"
              label="Create Account"
              size="lg"
              class="full-width q-mt-md"
            />

            <div class="text-center q-mt-md text-grey-5">
              Already have an account?
              <router-link to="/login" class="text-primary" style="text-decoration: none"
                >Log In</router-link
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

const name = ref('')
const email = ref('')
const password = ref('')
const confirmPassword = ref('')
const agree = ref(false)
</script>
