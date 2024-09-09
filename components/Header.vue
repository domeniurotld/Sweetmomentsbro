<template>
  <header class="header">
    <div class="row desktop-only">
      <nav class="nav nav-left">
        <button class="tab-button" @click="scrollToTop()">Acasă</button>
        <button class="tab-button" @click="scrollToSection('products')">Produse</button>
        <button class="tab-button" @click="scrollToSection('aboutus')">Despre noi</button>
        <button class="tab-button" @click="scrollToSection('contact')">Contact</button>
      </nav>
      <div class="logo">
        <img src="/assets/logos/sweetmoments1_white.png" alt="Logo" @click="goToRoute('/')"/>
      </div>
      <nav class="nav nav-right">
        <button class="social-button">
          <img src="/assets/logos/facebook-logo.png" alt="Facebook" />
        </button>
        <button class="social-button">
          <img src="/assets/logos/instagram-logo.png" alt="Instagram" />
        </button>
        <button class="social-button">
          <img src="/assets/logos/twitterx-logo.png" alt="Twitter" />
        </button>
      </nav>
    </div>

    <div class="mobile-only">
      <div class="logo" style="justify-content: center; display: flex;">
        <img src="/assets/logos/sweetmoments1_white.png" alt="Logo" />
      </div>
      <div class="col">
        <nav class="nav nav-left">
          <button class="tab-button" @click="scrollToTop()">Acasă</button>
          <button class="tab-button" @click="scrollToSection('products')">Produse</button>
          <button class="tab-button" @click="scrollToSection('aboutus')">Despre noi</button>
          <button class="tab-button" @click="scrollToSection('contact')">Contact</button>
        </nav>
        <nav class="nav nav-right">
          <button class="social-button">
            <img src="/assets/logos/facebook-logo.png" alt="Facebook" />
          </button>
          <button class="social-button">
            <img src="/assets/logos/instagram-logo.png" alt="Instagram" />
          </button>
          <button class="social-button">
            <img src="/assets/logos/twitterx-logo.png" alt="Twitter" />
          </button>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    goToRoute(route) {
      this.$router.push(route);
    },
    scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  }
}
</script>

<style scoped>
  @media (min-width: 1300px) {
      .header {
          padding-left: 14rem !important;
          padding-right: 14rem !important;
      }
  }

  .desktop-only {
    width:100%; 
    flex-direction:row; 
    display: flex;
  }

  .mobile-only {
    display: none; 
  }

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 1.5rem;
  background-color: #ef859c;
  height: auto;
}

.logo img {
  height: 100px;
  cursor: pointer;
}

.nav {
  display: flex;
  gap: 1rem;
}

.nav-left {
  flex: 1;
}

.nav-right {
  flex: 1;
  justify-content: flex-end;
}

.tab-button, .social-button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  color: white;
}

.tab-button {
  font-size: 1.2rem;
}

.social-button img {
  height: 26px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .desktop-only {
    display: none;
  }

  .mobile-only {
    width: 100%; 
    display: flex; 
    flex-direction: column;
  }

  .header {
    flex-direction: column;
    align-items: center;
    padding: 0 1rem;
  }

  .nav {
    width: 100%;
    justify-content: center;
    margin-bottom: 0.6rem;
  }

  .nav-left, .nav-right {
    align-items: center;
  }

  .tab-button {
    font-size: 1.1rem;
  }

  .social-button img {
    height: 23px;
  }
}
</style>
