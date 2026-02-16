<template>
  <nav>
  <div class="logo">
  <img src="@/Images/logo.jpg" alt="Logo" class="logo-img" />
  <span>Thanalakshmi Paulraj</span>
</div>

    <ul>
      <li>
        <a 
          href="#experience-section" 
          :class="{ 'active': activeSection === 'experience-section' }"
          @click="scrollToSection('experience-section', $event)"
        >
          Experience
        </a>
      </li>
      <li>
        <a 
          href="#projects" 
          :class="{ 'active': activeSection === 'projects' }"
          @click="scrollToSection('projects', $event)"
        >
          Projects
        </a>
      </li>
      <li>
        <a 
          href="#contacts" 
          :class="{ 'active': activeSection === 'contacts' }"
          @click="scrollToSection('contacts', $event)"
        >
          Contacts
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      activeSection: ''
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
    // Set initial active section
    this.handleScroll()
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      const sections = ['experience-section', 'projects', 'contacts']
      const scrollPosition = window.scrollY + 100 // Offset for navbar height
      
      for (let i = sections.length - 1; i >= 0; i--) {
        const section = document.getElementById(sections[i])
        if (section) {
          const sectionTop = section.offsetTop
          const sectionHeight = section.offsetHeight
          
          if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
            this.activeSection = sections[i]
            break
          }
        }
      }
      
      // If at top of page, no section is active
      if (scrollPosition < 200) {
        this.activeSection = ''
      }
    },
    scrollToSection(sectionId, event) {
      event.preventDefault()
      const section = document.getElementById(sectionId)
      if (section) {
        const navHeight = 80 // Approximate navbar height
        const sectionTop = section.offsetTop - navHeight
        
        window.scrollTo({
          top: sectionTop,
          behavior: 'smooth'
        })
      }
    }
  }
}
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background: white;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

.logo {
  font-size: 23px;
  font-weight: 600;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 30px;
}

nav a {
  text-decoration: none;
  color: #333;
  font-size: 18px;
  transition: all 0.3s;
  position: relative;
  padding: 5px 0;
}

nav a:hover {
  color: #FDB515;
}

/* Active link styles */
nav a.active {
  color: #FDB515;
  font-weight: 600;
}

/* Animated underline for active link */
nav a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 3px;
  background: linear-gradient(90deg, #FDB515, #f59e0b);
  border-radius: 2px;
  transition: width 0.3s ease;
}

nav a.active::after {
  width: 100%;
}

nav a:hover::after {
  width: 100%;
}

@media (max-width: 768px) {
  nav {
    padding: 20px;
  }
  
  nav ul {
    gap: 15px;
  }
  
  nav a {
    font-size: 16px;
  }
}
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 23px;
  font-weight: 600;
}

.logo-img {
  width: 35px;
  height: 35px;
  object-fit: contain;
}

</style>