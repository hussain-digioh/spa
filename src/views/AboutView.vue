<template>
  <div>
    <!-- Mission -->
    <section class="section">
      <div class="container mission-block">
        <div class="mission-text">
          <h2 class="section-title">We help brands know their customers</h2>
          <p class="mission-body">
            Digioh is the #1 zero-party data platform for ecommerce. We help brands collect
            meaningful customer preferences through quizzes, forms, and progressive profiling —
            then put that data to work across every channel.
          </p>
          <p class="mission-body">
            Since 2012, thousands of brands have used Digioh to grow email lists, power
            personalized product recommendations, and drive measurable revenue growth without
            relying on third-party cookies.
          </p>
          <a href="https://www.digioh.com" target="_blank" class="btn btn-primary">Visit digioh.com</a>
        </div>
        <div class="mission-badge">
          <span class="badge-number">2012</span>
          <span class="badge-label">Founded</span>
        </div>
      </div>
    </section>

    <!-- Stats -->
    <section class="section bg-navy">
      <div class="container">
        <div class="stats-grid">
          <div class="stat-item" v-for="stat in stats" :key="stat.label">
            <span class="stat-value">{{ stat.value }}</span>
            <span class="stat-label">{{ stat.label }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Product -->
    <section class="section bg-light">
      <div class="container">
        <h2 class="section-title">What we offer</h2>
        <p class="section-subtitle">A full suite of tools built for modern ecommerce teams.</p>
        <div class="product-grid">
          <div class="product-card" v-for="p in products" :key="p.name">
            <div class="product-icon">{{ p.icon }}</div>
            <h3 class="product-name">{{ p.name }}</h3>
            <p class="product-desc">{{ p.desc }}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const stats = [
  { value: '10,000+', label: 'Brands trust Digioh' },
  { value: '500M+', label: 'Profiles collected' },
  { value: '99.9%', label: 'Platform uptime' },
  { value: '3.2×', label: 'Average revenue lift' },
]

const products = [
  {
    icon: '📋',
    name: 'Quizzes & Forms',
    desc: 'Build interactive quizzes that capture zero-party data and guide shoppers to the right products.',
  },
  {
    icon: '🪟',
    name: 'Overlays & Lightboxes',
    desc: 'High-converting popups and slide-ins triggered by behavior, scroll, and exit intent.',
  },
  {
    icon: '🧩',
    name: 'Embedded Widgets',
    desc: 'Inline content blocks placed anywhere on your site using the universal smart tag.',
  },
  {
    icon: '📬',
    name: 'Email List Growth',
    desc: 'Grow your list with consent-first captures that integrate directly into your ESP.',
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

/* Mission */
.mission-block {
  display: flex;
  align-items: center;
  gap: 64px;
  flex-wrap: wrap;
}

.mission-text {
  flex: 1;
  min-width: 280px;
}

.mission-body {
  color: var(--dg-text-muted);
  line-height: 1.8;
  margin-bottom: 20px;
}

.mission-badge {
  flex-shrink: 0;
  width: 140px;
  height: 140px;
  border-radius: 50%;
  background: var(--dg-orange);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: var(--dg-white);
  box-shadow: 0 8px 32px rgba(2, 104, 106, 0.35);
}

.badge-number {
  font-size: 1.8rem;
  font-weight: 800;
  line-height: 1;
}

.badge-label {
  font-size: 0.8rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  opacity: 0.85;
  margin-top: 4px;
}

/* Stats */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 32px;
  text-align: center;
}

.stat-item {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.stat-value {
  font-size: 2.2rem;
  font-weight: 800;
  color: var(--dg-orange);
  line-height: 1;
}

.stat-label {
  font-size: 0.9rem;
  color: rgba(255, 255, 255, 0.65);
  font-weight: 500;
}

/* Products */
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  gap: 24px;
}

.product-card {
  background: var(--dg-white);
  border: 1px solid var(--dg-border);
  border-radius: 12px;
  padding: 28px 24px;
  transition: box-shadow 0.2s, transform 0.2s;
}

.product-card:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
  transform: translateY(-2px);
}

.product-icon {
  font-size: 1.8rem;
  margin-bottom: 14px;
}

.product-name {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--dg-navy);
  margin-bottom: 8px;
}

.product-desc {
  font-size: 0.92rem;
  color: var(--dg-text-muted);
  line-height: 1.7;
}
</style>
