<template>
  <div class="app">
    <header class="nav">
      <div class="container nav-inner">
        <RouterLink to="/" class="nav-logo">
          <span class="nav-logo-dot"></span>
          Digioh QA
        </RouterLink>
        <nav class="nav-links">
          <RouterLink to="/home" class="nav-link" active-class="nav-link--active">Home</RouterLink>
          <RouterLink to="/about" class="nav-link" active-class="nav-link--active">About</RouterLink>
        </nav>
      </div>
    </header>

    <main>
      <RouterView />
    </main>

    <footer class="footer">
      <div class="container footer-inner">
        <span>© 2026 Digioh SPA QA &mdash; powered by <a href="https://www.digioh.com" target="_blank">Digioh</a></span>
      </div>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped>
/* display:contents flattens this div so nav/main/footer become
   direct flex children of body and can be ordered around #digioh-host */
.app {
  display: contents;
}

/* Nav */
.nav {
  order: 1;
  position: sticky;
  top: 0;
  z-index: 100;
  background: var(--dg-navy);
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.25);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 64px;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--dg-white);
  letter-spacing: 0.5px;
}

.nav-logo-dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--dg-orange);
  display: inline-block;
}

.nav-links {
  display: flex;
  gap: 8px;
}

.nav-link {
  color: rgba(255, 255, 255, 0.7);
  padding: 8px 16px;
  border-radius: 6px;
  font-weight: 500;
  font-size: 0.95rem;
  transition: color 0.2s, background 0.2s;
}

.nav-link:hover,
.nav-link--active {
  color: var(--dg-white);
  background: rgba(2, 104, 106, 0.2);
}

.nav-link--active {
  color: var(--dg-orange);
}

/* Main */
main {
  order: 3;
  flex: 1;
}

/* Footer */
.footer {
  order: 4;
  background: var(--dg-navy);
  color: rgba(255, 255, 255, 0.55);
  font-size: 0.875rem;
  padding: 20px 0;
}

.footer-inner {
  display: flex;
  justify-content: center;
}

.footer a {
  color: var(--dg-orange);
}

.footer a:hover {
  text-decoration: underline;
}
</style>
