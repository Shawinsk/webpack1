<template>
  <q-page class="bg-dark text-white q-pa-xl">
    <div class="text-center q-mb-xl">
      <div class="text-overline text-primary text-weight-bold tracking-widest">SIMPLE PRICING</div>
      <h1 class="text-h2 text-weight-bold q-mb-md">Choose the right plan for you</h1>
      <p class="text-grey-4 text-h6">Transparent pricing with no hidden fees.</p>
    </div>

    <div class="row justify-center q-gutter-lg items-stretch">
      <div class="col-12 col-md-3" v-for="plan in plans" :key="plan.name">
        <q-card
          class="text-white column full-height no-shadow border-red feature-card"
          style="background-color: #121212"
          :class="{ 'highlight-plan': plan.popular }"
        >
          <q-item v-if="plan.popular" class="bg-primary text-center q-py-xs">
            <q-item-section
              ><div class="text-caption text-weight-bold">MOST POPULAR</div></q-item-section
            >
          </q-item>
          <q-card-section class="q-pa-lg text-center col-grow">
            <div class="text-h5 text-weight-bold q-mb-sm">{{ plan.name }}</div>
            <div class="text-h3 text-primary text-weight-bolder q-mb-lg">
              ${{ plan.price }}<span class="text-h6 text-grey-5">/mo</span>
            </div>
            <p class="text-grey-4 text-caption q-mb-md">{{ plan.desc }}</p>

            <q-separator color="grey-8" class="q-mb-md" />

            <q-list dense class="text-left">
              <q-item v-for="feature in plan.features" :key="feature" class="q-px-none">
                <q-item-section avatar style="min-width: 30px">
                  <q-icon name="check_circle" color="primary" size="xs" />
                </q-item-section>
                <q-item-section class="text-grey-4">{{ feature }}</q-item-section>
              </q-item>
            </q-list>
          </q-card-section>

          <q-card-actions align="center" class="q-pa-lg">
            <q-btn
              :outline="!plan.popular"
              :unelevated="plan.popular"
              color="primary"
              text-color="white"
              class="full-width rounded-borders"
              :label="plan.buttonText"
            />
          </q-card-actions>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
const plans = [
  {
    name: 'Starter',
    price: '0',
    desc: 'Perfect for freelancers and individuals getting started.',
    buttonText: 'Start for Free',
    popular: false,
    features: ['Up to 500 Contacts', 'Basic Pipeline', 'Email Support', 'Mobile App Access'],
  },
  {
    name: 'Professional',
    price: '29',
    desc: 'Ideal for growing teams that need more power.',
    buttonText: 'Get Started',
    popular: true,
    features: [
      'Unlimited Contacts',
      'Automated Workflows',
      'Advanced Reporting',
      'Priority Support',
      'Email Integration',
    ],
  },
  {
    name: 'Enterprise',
    price: '99',
    desc: 'For large organizations needing advanced control.',
    buttonText: 'Contact Sales',
    popular: false,
    features: [
      'Dedicated Account Manager',
      'Custom API Access',
      'SSO & Advanced Security',
      'Unlimited Pipelines',
      'Onboarding Assistance',
    ],
  },
]
</script>

<style scoped>
.feature-card {
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  transition: transform 0.3s;
}
.feature-card:hover {
  transform: translateY(-5px);
  border-color: var(--q-primary);
}
.highlight-plan {
  border: 2px solid var(--q-primary);
  transform: scale(1.05);
  box-shadow: 0 0 20px rgba(213, 0, 0, 0.2);
}
.highlight-plan:hover {
  transform: scale(1.05) translateY(-5px);
}
</style>
