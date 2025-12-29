<template>
  <q-page class="bg-dark text-white q-pa-xl">
    <div class="container" style="max-width: 1000px; margin: 0 auto">
      <div class="text-center q-mb-xl">
        <div class="text-overline text-primary text-weight-bold tracking-widest">
          POWERFUL TOOLS
        </div>
        <h1 class="text-h2 text-weight-bold q-mb-md">Features that empower your business</h1>
        <p class="text-grey-4 text-h6">
          Explore the capabilities that make our CRM the preferred choice for enterprises.
        </p>
      </div>

      <div class="q-gutter-y-xl">
        <div
          class="row items-center q-col-gutter-xl"
          v-for="(feature, index) in featureList"
          :key="index"
          :class="{ reverse: index % 2 === 1 }"
        >
          <div class="col-12 col-md-6">
            <div
              class="q-pa-md rounded-borders border-red relative-position"
              style="height: 300px; overflow: hidden; background-color: #121212"
            >
              <!-- Placeholder for feature image/graphic -->
              <div class="absolute-full flex flex-center bg-grey-9 text-grey-7">
                <q-icon :name="feature.icon" size="100px" color="primary" style="opacity: 0.5" />
              </div>
            </div>
          </div>
          <div class="col-12 col-md-6">
            <h3 class="text-h4 text-weight-bold q-mb-sm">{{ feature.title }}</h3>
            <p class="text-grey-4 text-body1 q-mb-lg">{{ feature.desc }}</p>
            <ul class="q-pl-md text-grey-4">
              <li v-for="item in feature.points" :key="item" class="q-mb-sm">{{ item }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
const featureList = [
  {
    title: 'Advanced Lead Tracking',
    icon: 'track_changes',
    desc: 'Never lose track of a potential customer. Our advanced tracking system logs every interaction automatically.',
    points: [
      'Automatic interaction logging',
      'Lead scoring and qualification',
      'Visual pipeline management',
    ],
  },
  {
    title: 'Automated Workflows',
    icon: 'settings_suggest',
    desc: 'Save time and reduce errors by automating repetitive tasks. Set up triggers and actions with ease.',
    points: ['Email follow-up sequences', 'Task assignment automation', 'Custom trigger events'],
  },
  {
    title: 'Deep Analytics',
    icon: 'analytics',
    desc: 'Make data-driven decisions with our comprehensive reporting tools. Customize dashboards to see what matters to you.',
    points: [
      'Real-time performance metrics',
      'Customizable report builder',
      'Export data to CSV/PDF',
    ],
  },
]
</script>

<style scoped>
.border-red {
  border: 1px solid rgba(213, 0, 0, 0.2);
}
</style>
