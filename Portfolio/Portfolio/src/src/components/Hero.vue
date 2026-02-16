<template>
  <section class="hero">
    <div class="hero-bg" :style="{ background: currentGradient }"></div>
    <div class="hero-content" data-aos="fade-right">
      <h1>Hello, My Name is Thanalakshmi</h1>

      <!-- Typing Effect Line -->
      <h2 class="typing-text">
        I'm a <span>{{ displayedText }}</span><span class="cursor"></span>
      </h2>

      <!-- Short Bio -->
      <p class="hero-bio">
        Passionate Frontend Developer with 1.7 years of experience specializing in Vue.js and React.js. 
        I create intuitive, responsive web applications that deliver seamless user experiences.
      </p>

      <div class="hero-buttons">
        <a href="#projects" class="btn btn-primary">View Projects</a>
        <a href="https://www.linkedin.com/in/thanalakshmi-p" target="_blank" class="btn btn-secondary">LinkedIn</a>
      </div>
    </div>
    <div class="hero-image" data-aos="fade-left" data-aos-delay="200">
      <!-- Tech Stack Icons Behind Image -->
      <div class="tech-stack-background">
        <!-- Left side icons -->
        <div class="tech-icon floating" style="top: 15%; left: 5%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" alt="Vue.js">
          <div class="tooltip-box">
    <span class="tech-name">Vue</span>
  </div>
        </div>
        <div class="tech-icon floating" style="top: 40%; left: 5%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript">
          <div class="tooltip-box">
    <span class="tech-name">JavaScript</span>
  </div>
        </div>
        <div class="tech-icon floating" style="bottom: 20%; left: 5%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5">
          <div class="tooltip-box">
    <span class="tech-name">Html</span>
  </div>
        </div>
        
        <!-- Right side icons -->
        <!-- <div class="tech-icon floating" style="top: 15%; right: -12%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">
        </div> -->
        <div class="tech-icon floating" style="top: 15%; right: -12%;">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">

  <div class="tooltip-box">
    <span class="tech-name">React</span>
  </div>
</div>

        <div class="tech-icon floating" style="top: 40%; right: -15%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3">
           <div class="tooltip-box">
    <span class="tech-name">CSS3</span>
  </div>
        </div>
        <div class="tech-icon floating" style="bottom: 20%; right: -12%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" alt="Bootstrap">
           <div class="tooltip-box">
    <span class="tech-name">Bootstrap</span>
  </div>
        </div>
        
        <!-- Top and Bottom icons -->
        <div class="tech-icon floating" style="bottom: -1%; right:-15%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" alt="Tailwind CSS">
          <div class="tooltip-box">
    <span class="tech-name">Tailwind</span>
  </div>
        </div>
        <div class="tech-icon floating" style="bottom: -1%; left: 15%;">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git">
          <div class="tooltip-box">
    <span class="tech-name">Git</span>
  </div>
        </div>
      </div>
      
      <div class="yellow-blob" :style="{ background: currentColor }"></div>
      <img src="../Images/Background (1).jpg" alt="Thanalakshmi Paulraj" class="hero-photo">
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero',
  data() {
    return {
      roles: [
        { text: "Frontend Developer", color: "#FF6B6B" },
        { text: "UI/UX Designer", color: "#4ECDC4" },
        { text: "React Enthusiast", color: "#1A535C" },
        { text: "Vue.js Specialist", color: "#FFCA3A" },
        { text: "Web Performance Optimizer", color: "#6A4C93" }
      ],
      displayedText: '',
      wordIndex: 0,
      charIndex: 0,
      deleting: false,
      currentColor: '#FDB515',
      currentGradient: 'linear-gradient(120deg, #FDB515, #FEBA13)',
      TYPING_SPEED: 80,
      DELETING_SPEED: 40,
      PAUSE_AFTER: 1400,
      PAUSE_BEFORE: 400,
      timeout: null
    }
  },
  mounted() {
    setTimeout(() => {
      this.tick()
    }, 500)
  },
  beforeDestroy() {
    if (this.timeout) {
      clearTimeout(this.timeout)
    }
  },
  methods: {
    tick() {
      const current = this.roles[this.wordIndex].text
      
      if (!this.deleting) {
        this.charIndex++
        this.displayedText = current.slice(0, this.charIndex)
        
        if (this.charIndex === current.length) {
          this.deleting = true
          this.currentGradient = `linear-gradient(120deg, ${this.roles[this.wordIndex].color}, #fff)`
          this.currentColor = this.roles[this.wordIndex].color
          this.timeout = setTimeout(() => this.tick(), this.PAUSE_AFTER)
          return
        }
        this.timeout = setTimeout(() => this.tick(), this.TYPING_SPEED)
      } else {
        this.charIndex--
        this.displayedText = current.slice(0, this.charIndex)
        
        if (this.charIndex === 0) {
          this.deleting = false
          this.wordIndex = (this.wordIndex + 1) % this.roles.length
          this.timeout = setTimeout(() => this.tick(), this.PAUSE_BEFORE)
          return
        }
        this.timeout = setTimeout(() => this.tick(), this.DELETING_SPEED)
      }
    }
  }
}
</script>

<style scoped>
.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 60px;
  padding: 40px 40px;
  min-height: 85vh;
  background: #fff;
  max-width: 1200px;
  margin: 0 auto;
}

.hero-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  transition: all 0.8s ease;
  filter: blur(80px);
  opacity: 0.5;
}

.hero-content {
  flex: 1;
  max-width: 500px;
  z-index: 2;
}

.hero h1 {
  font-size: 38px;
  margin-bottom: 15px;
  line-height: 1.2;
}

.typing-text {
  font-size: 22px;
  font-weight: 500;
  margin-bottom: 20px;
}

.hero-bio {
  font-size: 16px;
  line-height: 1.7;
  color: #555;
  margin-bottom: 25px;
  max-width: 500px;
}

/* Tech Stack Icons */
.tech-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 30px;
}

.tech-stack-background {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.tech-icon {
  position: absolute;
  width: 55px;
  height: 55px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: white;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
  transition: all 0.3s ease;
  cursor: pointer;
}

.tech-icon.floating {
  animation: float 3s ease-in-out infinite;
}

.tech-icon.floating:nth-child(1) { animation-delay: 0s; }
.tech-icon.floating:nth-child(2) { animation-delay: 0.2s; }
.tech-icon.floating:nth-child(3) { animation-delay: 0.4s; }
.tech-icon.floating:nth-child(4) { animation-delay: 0.6s; }
.tech-icon.floating:nth-child(5) { animation-delay: 0.8s; }
.tech-icon.floating:nth-child(6) { animation-delay: 1s; }
.tech-icon.floating:nth-child(7) { animation-delay: 1.2s; }
.tech-icon.floating:nth-child(8) { animation-delay: 1.4s; }

@keyframes float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-15px);
  }
}

.tech-icon:hover {
  transform: translateY(-8px) scale(1.1);
  box-shadow: 0 12px 35px rgba(0, 0, 0, 0.2);
  z-index: 10;
}

.tech-icon img {
  width: 35px;
  height: 35px;
  object-fit: contain;
}


.cursor {
  display: inline-block;
  width: 3px;
  background: #333;
  animation: blink 0.7s infinite;
  margin-left: 2px;
}

@keyframes blink {
  0%, 50%, 100% { opacity: 1; }
  25%, 75% { opacity: 0; }
}

.hero-buttons {
  display: flex;
  gap: 15px;
}

.btn {
  padding: 12px 30px;
  border: none;
  cursor: pointer;
  font-size: 14px;
  font-weight: 600;
  transition: all 0.3s;
  text-decoration: none;
  display: inline-block;
}

.btn-primary {
  background: #FDB515;
  color: white;
  border-radius: 4px;
}

.btn-primary:hover {
  background: #e5a213;
  transform: translateY(-2px);
}

.btn-secondary {
  background: white;
  color: #333;
  border: 2px solid #333;
  border-radius: 4px;
}

.btn-secondary:hover {
  background: #333;
  color: white;
}

.hero-image {
  position: relative;
  flex: 1;
  display: flex;
  justify-content: flex-end;
}

.yellow-blob {
  position: absolute;
  right: -100px;
  top: -100px;
  display: none;
  width: 600px;
  height: 600px;
  border-radius: 45% 55% 60% 40% / 50% 45% 55% 50%;
  z-index: 0;
  transition: all 0.5s ease;
}

.hero-photo {
  width: 380px;
  height: 480px;
  object-fit: cover;
  border-radius: 10px;
  z-index: 2;
  position: relative;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}
.tech-icon {
  position: absolute;
  background: #f5f5f5;
  padding: 12px;
  border-radius: 16px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.08);
  text-align: center;
  transition: transform 0.3s ease;
}

.tech-icon img {
  width: 40px;
}

/* Tooltip container */
.tooltip-box {
  position: absolute;
  bottom: 110%;
  left: 50%;
  transform: translateX(-50%) translateY(10px);
  opacity: 0;
  pointer-events: none;
  text-align: center;
  transition: all 0.4s cubic-bezier(.25,.8,.25,1);
}

/* Arrow */
.arrow {
  display: block;
  font-size: 14px;
  color: #333;
  transform: translateY(5px);
  transition: transform 0.4s ease;
}

/* Text */
.tech-name {
  background: #574952;
  color: #fff;
  padding: 5px 10px;
  border-radius: 8px;
  font-size: 12px;
  margin-top: 4px;
  display: inline-block;
}

/* Hover Effects */
.tech-icon:hover {
  transform: translateY(-5px);
}

.tech-icon:hover .tooltip-box {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}

.tech-icon:hover .arrow {
  transform: translateY(0);
}

</style>