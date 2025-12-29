<template>
  <q-page class="bg-dark text-white">
    <!-- Hero Section -->
    <section
      class="row items-center justify-center q-py-xl q-px-md hero-section"
      style="min-height: 80vh"
    >
      <div class="col-12 col-md-8 text-center">
        <div class="text-overline text-primary text-weight-bold q-mb-md tracking-widest">
          NEXT GEN MANAGEMENT
        </div>
        <h1 class="text-h2 text-md-h1 text-weight-bolder q-mb-lg leading-tight">
          Master Your <span class="text-primary">Customer<br />Relationships</span>
        </h1>
        <p
          class="text-h6 text-grey-4 q-mb-xl"
          style="max-width: 700px; margin-left: auto; margin-right: auto"
        >
          The all-in-one platform designed to help you organize conversations, convert leads, and
          scale your business effortlessly.
        </p>
        <div class="row justify-center q-gutter-md">
          <q-btn
            size="lg"
            rounded
            unelevated
            color="primary"
            text-color="white"
            label="Start Free Trial"
            class="q-px-xl"
          />
          <q-btn
            size="lg"
            rounded
            outline
            color="white"
            label="Watch Demo"
            icon="play_circle"
            class="q-px-xl"
          />
        </div>

        <!-- Dashboard Preview / Abstract Graphic -->
        <div class="q-mt-xl relative-position display-card">
          <q-img
            src="https://cdn.quasar.dev/img/parallax2.jpg"
            style="
              height: 400px;
              border-radius: 20px;
              opacity: 0.4;
              mask-image: linear-gradient(to bottom, black, transparent);
            "
            class="rounded-borders"
          >
            <div class="absolute-full flex flex-center">
              <q-icon name="dashboard" size="100px" color="primary" style="opacity: 0.8" />
              <div class="text-h4 text-weight-bold q-ml-md">Powerful Dashboard</div>
            </div>
          </q-img>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="q-py-xl bg-dark-page q-px-md">
      <div class="container" style="max-width: 1200px; margin: 0 auto">
        <div class="text-center q-mb-xl">
          <h2 class="text-h3 text-weight-bold q-mb-md">Why Choose Our CRM?</h2>
          <p class="text-grey-4 text-h6">
            Everything you need to manage your business in one place.
          </p>
        </div>

        <div class="row q-col-gutter-lg">
          <div class="col-12 col-md-4" v-for="feature in features" :key="feature.title">
            <q-card class="bg-dark text-white q-pa-md feature-card no-shadow border-red">
              <q-card-section>
                <div
                  class="row items-center justify-center q-mb-md bg-red-1 q-pa-sm"
                  style="
                    width: 60px;
                    height: 60px;
                    border-radius: 12px;
                    background: rgba(213, 0, 0, 0.1);
                  "
                >
                  <q-icon :name="feature.icon" color="primary" size="32px" />
                </div>
                <div class="text-h5 text-weight-bold q-mb-sm">{{ feature.title }}</div>
                <div class="text-grey-4">{{ feature.description }}</div>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </section>

    <!-- Statistics Section -->
    <section class="q-py-xl bg-primary text-white">
      <div
        class="container row justify-center text-center q-gutter-lg"
        style="max-width: 1200px; margin: 0 auto"
      >
        <div class="col-12 col-sm-3">
          <div class="text-h2 text-weight-bolder">10k+</div>
          <div class="text-subtitle1">Active Users</div>
        </div>
        <div class="col-12 col-sm-3">
          <div class="text-h2 text-weight-bolder">99%</div>
          <div class="text-subtitle1">Customer Satisfaction</div>
        </div>
        <div class="col-12 col-sm-3">
          <div class="text-h2 text-weight-bolder">24/7</div>
          <div class="text-subtitle1">Support Coverage</div>
        </div>
      </div>
    </section>

    <!-- Testimonials / Social Proof -->
    <section class="q-py-xl q-px-md bg-dark">
      <div class="text-center q-mb-xl">
        <div class="text-primary text-weight-bold q-mb-sm">TRUSTED BY TEAMS</div>
        <h2 class="text-h3 text-weight-bold">What our clients say</h2>
      </div>
      <div class="row justify-center q-gutter-lg">
        <q-card
          class="col-12 col-md-5 bg-dark-page text-white q-pa-lg no-shadow"
          style="border: 1px solid #333; border-radius: 16px"
        >
          <q-card-section>
            <div class="row items-center q-mb-md">
              <q-avatar size="50px" color="grey-8">
                <span class="text-h6">JD</span>
              </q-avatar>
              <div class="q-ml-md">
                <div class="text-bold">John Doe</div>
                <div class="text-grey-5 text-caption">CEO, TechCorp</div>
              </div>
            </div>
            <p class="text-grey-3 text-body1">
              "This CRM completely transformed how we handle our leads. The interface is stunning
              and the features are exactly what we needed."
            </p>
          </q-card-section>
        </q-card>
        <q-card
          class="col-12 col-md-5 bg-dark-page text-white q-pa-lg no-shadow"
          style="border: 1px solid #333; border-radius: 16px"
        >
          <q-card-section>
            <div class="row items-center q-mb-md">
              <q-avatar size="50px" color="grey-8">
                <span class="text-h6">AS</span>
              </q-avatar>
              <div class="q-ml-md">
                <div class="text-bold">Alice Smith</div>
                <div class="text-grey-5 text-caption">Marketing Director, CreativeCo</div>
              </div>
            </div>
            <p class="text-grey-3 text-body1">
              "The dark mode design is beautiful and easy on the eyes. Functionality wise, it's top
              notch. Highly recommended!"
            </p>
          </q-card-section>
        </q-card>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="q-py-xl bg-dark-page text-center q-px-md">
      <h2 class="text-h3 text-weight-bold q-mb-lg">Ready to grow your business?</h2>
      <p class="text-grey-4 text-h6 q-mb-xl">
        Join thousands of businesses managing their customers better.
      </p>
      <q-btn
        size="xl"
        rounded
        push
        color="primary"
        label="Get Started Now"
        class="q-px-xl text-weight-bold"
      />
    </section>
  </q-page>
</template>

<script setup>
const features = [
  {
    title: 'Lead Management',
    icon: 'person_add',
    description:
      'Capture, organize, and nurture leads to convert them into loyal customers efficiently.',
  },
  {
    title: 'Sales Pipeline',
    icon: 'trending_up',
    description:
      'Visualize your sales process and track deals from opportunity to close with ease.',
  },
  {
    title: 'Analytics & Reports',
    icon: 'insights',
    description:
      'Gain actionable insights into your performance with detailed, real-time analytics dashboards.',
  },
  {
    title: 'Email Integration',
    icon: 'email',
    description:
      'Seamlessly integrate with your email provider to track conversations and automate follow-ups.',
  },
  {
    title: 'Task Automation',
    icon: 'auto_mode',
    description:
      'Automate repetitive tasks and focus on what matters most - building relationships.',
  },
  {
    title: 'Team Collaboration',
    icon: 'groups',
    description:
      'Share notes, tasks, and files with your team to ensure everyone is on the same page.',
  },
]
</script>

<style scoped>
.hero-section {
  background: radial-gradient(circle at 50% 10%, rgba(213, 0, 0, 0.15) 0%, rgba(0, 0, 0, 0) 50%);
}

.feature-card {
  transition:
    transform 0.3s ease,
    border-color 0.3s ease;
  border: 1px solid transparent;
  background: rgba(255, 255, 255, 0.03);
}

.feature-card:hover {
  transform: translateY(-5px);
  border-color: var(--q-primary);
  background: rgba(213, 0, 0, 0.05);
}

.border-red {
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.text-h1,
.text-h2,
.text-h3 {
  letter-spacing: -1px;
}
</style>
