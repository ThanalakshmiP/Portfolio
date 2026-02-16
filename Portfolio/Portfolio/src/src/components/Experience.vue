Copy

<template>
  <section class="experience-section" id="experience-section">
    <h2 data-aos="fade-up">Professional Experience</h2>
    <p class="experience-subtitle" data-aos="fade-up" data-aos-delay="100">My journey in building impactful web applications</p>
   
    <div class="experience-container">
      <div class="timeline">
        <!-- Experience Item -->
        <div 
          v-for="(experience, index) in experiences"
          :key="index"
          class="timeline-item"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="timeline-dot"></div>
          <div class="experience-card">
            <div class="experience-header">
              <div class="company-name">{{ experience.company }}</div>
              <div class="job-title">{{ experience.title }}</div>
              <div class="duration">{{ experience.duration }}</div>
            </div>
            <div class="experience-description">
              {{ experience.description }}
            </div>
            <div class="experience-tech">
              <span 
                v-for="(tech, techIndex) in experience.technologies" 
                :key="techIndex"
                class="tech-badge"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Experience',
  data() {
    return {
   experiences: [
        {
          company: 'Datayaan solutions Private Limited',
          title: ' Software Engineer - Junior Frontend Developer',
          duration: 'July 2024 - Present · 1.7 yrs Experience',
          description: 'Led the development of multiple healthcare management systems, focusing on creating intuitive user interfaces and seamless user experiences for medical professionals and patients.',
          technologies: ['Vue.js','React.js','JavaScript', 'Vuex', 'REST APIs', 'Bootstrap', 'Axios','Responsive Web Design','Twilio']
        },
      ]
    }
  }
}
</script>

<style scoped>
.experience-section {
  padding: 13px 28px;
  margin: 30px;
  background: #f9f9f9;
}

.experience-section h2 {
  text-align: center;
  font-size: 42px;
  margin-bottom: 10px;
}

.experience-subtitle {
  text-align: center;
  font-size: 18px;
  font-weight: 500;
  color: #666;
  margin-bottom: 15px;
}

.experience-container {
  max-width: 1000px;
  margin: 0 auto;
  position: relative;
}

.timeline {
  position: relative;
  padding: 0;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 4px;
  height: 100%;
  background: linear-gradient(180deg, #FDB515, #667eea);
  border-radius: 2px;
}

.timeline-item {
  position: relative;
  margin-bottom: 50px;
  width: 100%;
}

.timeline-item:nth-child(odd) .experience-card {
  margin-left: 0;
  margin-right: auto;
  padding-right: 40px;
}

.timeline-item:nth-child(even) .experience-card {
  margin-left: auto;
  margin-right: 0;
  padding-left: 40px;
}

.experience-card {
  background: white;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  width: calc(50% - 30px);
  position: relative;
  transition: all 0.3s ease;
  cursor: pointer;
}

.experience-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 30px rgba(0,0,0,0.15);
}

.timeline-dot {
  position: absolute;
  top: 30px;
  left: 50%;
  transform: translateX(-50%);
  width: 20px;
  height: 20px;
  background: #FDB515;
  border: 4px solid white;
  border-radius: 50%;
  box-shadow: 0 0 0 4px rgba(253, 181, 21, 0.2);
  z-index: 2;
  transition: all 0.3s ease;
}

.timeline-item:hover .timeline-dot {
  transform: translateX(-50%) scale(1.3);
  box-shadow: 0 0 0 8px rgba(253, 181, 21, 0.3);
}

.experience-header {
  margin-bottom: 20px;
}

.company-name {
  font-size: 24px;
  font-weight: 700;
  color: #222;
  margin-bottom: 5px;
}

.job-title {
  font-size: 18px;
  color: #667eea;
  font-weight: 600;
  margin-bottom: 5px;
}

.duration {
  font-size: 14px;
  color: #999;
  display: flex;
  align-items: center;
  gap: 5px;
}

.duration::before {
  content: '📅';
}

.experience-description {
  color: #666;
  font-size: large;
  line-height: 1.8;
  margin-bottom: 15px;
}

.experience-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.tech-badge {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 5px 12px;
  border-radius: 20px;
  font-size: 13px;
  font-weight: 600;
}
</style>