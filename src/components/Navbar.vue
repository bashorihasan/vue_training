<template>
  <nav class="navbar" :class="{ scrolled: isScrolled }">
    <div class="container">
      <div class="logo">
        <h2>{{ companyName }}</h2>
      </div>
      <ul class="nav-menu" :class="{ active: mobileMenuOpen }">
        <li><a href="#home" @click="closeMenu">Home</a></li>
        <li><a href="#about" @click="closeMenu">About</a></li>
        <li><a href="#services" @click="closeMenu">Services</a></li>
        <li><a href="#team" @click="closeMenu">Team</a></li>
        <li><a href="#contact" @click="closeMenu">Contact</a></li>
      </ul>
      <div class="hamburger" @click="toggleMenu" :class="{ active: mobileMenuOpen }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      companyName: 'TechVision',
      isScrolled: false,
      mobileMenuOpen: false
    }
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50
    },
    toggleMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    closeMenu() {
      this.mobileMenuOpen = false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: transparent;
  padding: 20px 0;
  z-index: 1000;
  transition: all 0.3s ease;
}

.navbar.scrolled {
  background: rgba(255, 255, 255, 0.98);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 15px 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo h2 {
  color: #fff;
  font-size: 28px;
  font-weight: 700;
  transition: color 0.3s ease;
}

.navbar.scrolled .logo h2 {
  color: #2c3e50;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 30px;
}

.nav-menu li a {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
  font-size: 16px;
  transition: all 0.3s ease;
  position: relative;
}

.navbar.scrolled .nav-menu li a {
  color: #2c3e50;
}

.nav-menu li a:hover {
  color: #3498db;
}

.nav-menu li a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #3498db;
  transition: width 0.3s ease;
}

.nav-menu li a:hover::after {
  width: 100%;
}

.hamburger {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 5px;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background: #fff;
  transition: all 0.3s ease;
}

.navbar.scrolled .hamburger span {
  background: #2c3e50;
}

@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-menu {
    position: fixed;
    left: -100%;
    top: 70px;
    flex-direction: column;
    background: rgba(255, 255, 255, 0.98);
    width: 100%;
    text-align: center;
    transition: 0.3s;
    box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
    padding: 20px 0;
  }

  .nav-menu.active {
    left: 0;
  }

  .nav-menu li a {
    color: #2c3e50;
    padding: 10px 0;
    display: block;
  }

  .hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(8px, 8px);
  }

  .hamburger.active span:nth-child(2) {
    opacity: 0;
  }

  .hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(8px, -8px);
  }
}
</style>
