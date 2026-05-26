<template>
  <div>
    <!-- Features Section -->
    <section class="section bg-light">
      <div class="container">
        <h2 class="section-title">Why Digioh?</h2>
        <p class="section-subtitle">The complete platform for personalized ecommerce experiences.</p>
        <div class="feature-grid">
          <div class="feature-card" v-for="f in features" :key="f.title">
            <div class="feature-icon">{{ f.icon }}</div>
            <h3 class="feature-title">{{ f.title }}</h3>
            <p class="feature-desc">{{ f.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section class="section">
      <div class="container">
        <h2 class="section-title">How it works</h2>
        <p class="section-subtitle">Three steps to smarter customer engagement.</p>
        <div class="steps">
          <div class="step" v-for="(step, i) in steps" :key="step.label">
            <div class="step-number">{{ i + 1 }}</div>
            <div>
              <h4 class="step-label">{{ step.label }}</h4>
              <p class="step-desc">{{ step.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA -->
    <section class="section bg-navy">
      <div class="container cta-block">
        <h2 class="cta-title">Ready to convert more visitors?</h2>
        <p class="cta-sub">Launch your first personalized campaign in minutes.</p>
        <div class="cta-actions">
          <a href="https://www.digioh.com" target="_blank" class="btn btn-primary">Get started free</a>
          <RouterLink to="/about" class="btn btn-outline-white">Learn more</RouterLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const features = [
  {
    icon: '🎯',
    title: 'Personalization',
    desc: 'Serve the right message to the right visitor based on behavior, source, and intent.',
  },
  {
    icon: '⚡',
    title: 'Zero Page Impact',
    desc: 'Async loading means your core web vitals are never affected by Digioh campaigns.',
  },
  {
    icon: '🧪',
    title: 'A/B Testing',
    desc: 'Run experiments on headlines, offers, and layouts with built-in traffic splitting.',
  },
  {
    icon: '📊',
    title: 'Analytics',
    desc: 'Real-time dashboards track impressions, conversions, and revenue attribution.',
  },
  {
    icon: '🔗',
    title: 'Integrations',
    desc: 'Connect to 100+ tools including Klaviyo, Salesforce, HubSpot, and Shopify.',
  },
  {
    icon: '🛡️',
    title: 'Compliance',
    desc: 'GDPR, CCPA, and CAN-SPAM ready with built-in consent management.',
  },
]

const steps = [
  {
    label: 'Install the snippet',
    desc: 'Drop a single async script tag into your site — no performance impact guaranteed.',
  },
  {
    label: 'Build your campaign',
    desc: 'Use the visual editor to design forms, quizzes, and overlays without writing code.',
  },
  {
    label: 'Set display conditions',
    desc: 'Target by URL, device, referrer, UTM, scroll depth, or any custom attribute.',
  },
]
</script>

<style scoped>
.bg-light {
  background: var(--dg-light);
}

.bg-navy {
  background: var(--dg-navy);
}

/* Features */
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 24px;
}

.feature-card {
  background: var(--dg-white);
  border: 1px solid var(--dg-border);
  border-radius: 12px;
  padding: 28px 24px;
  transition: box-shadow 0.2s, transform 0.2s;
}

.feature-card:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
  transform: translateY(-2px);
}

.feature-icon {
  font-size: 1.8rem;
  margin-bottom: 14px;
}

.feature-title {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--dg-navy);
  margin-bottom: 8px;
}

.feature-desc {
  font-size: 0.92rem;
  color: var(--dg-text-muted);
  line-height: 1.7;
}

/* Steps */
.steps {
  display: flex;
  flex-direction: column;
  gap: 28px;
  max-width: 640px;
}

.step {
  display: flex;
  align-items: flex-start;
  gap: 20px;
}

.step-number {
  flex-shrink: 0;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: var(--dg-orange);
  color: var(--dg-white);
  font-weight: 700;
  font-size: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.step-label {
  font-size: 1rem;
  font-weight: 700;
  color: var(--dg-navy);
  margin-bottom: 4px;
}

.step-desc {
  font-size: 0.92rem;
  color: var(--dg-text-muted);
  line-height: 1.7;
}

/* CTA */
.cta-block {
  text-align: center;
}

.cta-title {
  font-size: 2rem;
  font-weight: 700;
  color: var(--dg-white);
  margin-bottom: 12px;
}

.cta-sub {
  color: rgba(255, 255, 255, 0.65);
  font-size: 1.05rem;
  margin-bottom: 36px;
}

.cta-actions {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-outline-white {
  display: inline-block;
  padding: 12px 28px;
  border-radius: 6px;
  font-size: 0.95rem;
  font-weight: 600;
  border: 2px solid rgba(255, 255, 255, 0.5);
  color: var(--dg-white);
  transition: border-color 0.2s, background 0.2s;
}

.btn-outline-white:hover {
  border-color: var(--dg-white);
  background: rgba(255, 255, 255, 0.1);
}
</style>
