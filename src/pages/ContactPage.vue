<template>
  <q-page class="bg-dark text-white q-pa-xl flex flex-center">
    <div class="row full-width" style="max-width: 1100px">
      <div class="col-12 col-md-5 q-pr-md-xl q-mb-xl q-mb-md-none">
        <div class="text-overline text-primary text-weight-bold tracking-widest">GET IN TOUCH</div>
        <h1 class="text-h2 text-weight-bold q-mb-md">Let's start a conversation</h1>
        <p class="text-grey-4 text-h6 q-mb-xl">
          Have questions? We'd love to hear from you. customized solution or just want to say hi?
        </p>

        <div class="q-gutter-y-lg">
          <div class="row items-center">
            <q-avatar
              icon="location_on"
              color="primary"
              text-color="white"
              font-size="24px"
              class="q-mr-md"
            />
            <div>
              <div class="text-weight-bold">Headquarters</div>
              <div class="text-grey-4">123 Tech Avenue, Colombo 03, Sri Lanka</div>
            </div>
          </div>

          <div class="row items-center">
            <q-avatar
              icon="email"
              color="primary"
              text-color="white"
              font-size="24px"
              class="q-mr-md"
            />
            <div>
              <div class="text-weight-bold">Email Us</div>
              <div class="text-grey-4">hello@kdjweb.com</div>
            </div>
          </div>

          <div class="row items-center">
            <q-avatar
              icon="phone"
              color="primary"
              text-color="white"
              font-size="24px"
              class="q-mr-md"
            />
            <div>
              <div class="text-weight-bold">Call Us</div>
              <div class="text-grey-4">+94 11 234 5678</div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-12 col-md-7">
        <q-card
          class="text-white q-pa-lg no-shadow"
          style="border: 1px solid #333; border-radius: 16px; background-color: #121212"
        >
          <q-card-section>
            <div class="text-h5 text-weight-bold q-mb-lg">Send us a message</div>
            <q-form class="q-gutter-md">
              <div class="row q-col-gutter-md">
                <div class="col-12 col-sm-6">
                  <q-input dark outlined v-model="name" label="Your Name" color="primary" />
                </div>
                <div class="col-12 col-sm-6">
                  <q-input dark outlined v-model="email" label="Your Email" color="primary" />
                </div>
              </div>
              <q-input dark outlined v-model="subject" label="Subject" color="primary" />
              <q-input
                dark
                outlined
                v-model="message"
                label="Message"
                type="textarea"
                color="primary"
                rows="4"
              />

              <div class="text-right">
                <q-btn push color="primary" label="Send Message" size="lg" class="q-px-xl" />
              </div>
            </q-form>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const subject = ref('')
const message = ref('')
</script>
