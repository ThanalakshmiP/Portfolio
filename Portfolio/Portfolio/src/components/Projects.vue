<template>
  <section class="projects" id="projects">
    <h2 data-aos="fade-up">Projects</h2>

    <div 
      v-for="(project, index) in projects" 
      :key="index"
      class="project-card"
      :class="{ 'reverse': index % 2 === 1 }"
      data-aos="fade-up"
      :data-aos-delay="index * 150"
    >
      <img :src="project.image" :alt="project.title" class="project-image">
      <div class="project-info">
        <h3>{{ project.title }}</h3>
        <div class="tech-stack">
          <span 
            v-for="(tech, techIndex) in project.technologies" 
            :key="techIndex"
            class="tech-tag"
          >
            {{ tech }}
          </span>
        </div>
        <p>{{ project.description }}</p>
        <ul>
          <li v-for="(feature, featureIndex) in project.features" :key="featureIndex">
            {{ feature }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import gymImage from '@/Images/download.jpg'

export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'Pet Healthcare Application',
          image: 'https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?w=500&h=350&fit=crop',
          technologies: ['Vue.js', 'Vuex', 'REST APIs', 'Bootstrap', 'JavaScript'],
          description: 'A comprehensive pet healthcare platform designed to streamline clinic operations with five main modules: Admin, Doctor, Helpdesk, Patient, and Manager.',
          features: [
            'Developed responsive UI components following modular principles and UX best practices',
            'Integrated advanced features including appointment scheduling and health tracking',
            'Implemented e-commerce workflows with product browsing and cart management'
          ]
        },
        {
          title: 'Mobile Medical Unit',
          image: 'https://images.unsplash.com/photo-1584515933487-779824d29309?w=500&h=350&fit=crop',
          technologies: ['Vue.js', 'Vuex', 'REST APIs', 'Bootstrap', 'Axios'],
          description: 'A camp-based healthcare management system enhancing accessibility of medical services in remote areas with Admin, Doctor, Helpdesk, and Manager modules.',
          features: [
            'Built patient registration, appointment scheduling, and consultation tracking features',
            'Developed digital report management system for healthcare documentation',
            'Enhanced system usability by simplifying camp workflows for healthcare staff'
          ]
        },
        {
          title: 'E-Ambulance Management System',
          image: 'https://images.unsplash.com/photo-1587745416684-47953f16f02f?w=500&h=350&fit=crop',
          technologies: ['Vue.js', 'Vuex', 'REST APIs', 'JavaScript'],
          description: 'A real-time ambulance and emergency consultation platform with Admin, Paramedic, and Doctor modules for managing critical healthcare situations.',
          features: [
            'Engineered case booking flow where paramedics log details and doctors review cases',
            'Implemented ambulance tracking, emergency alerts, and role-based dashboards',
            'Integrated secure video call consultation for remote diagnosis and treatment'
          ]
        },
        {
  title: 'Athics Gym Management System',
  image: gymImage,
  technologies: ['Vue.js', 'Vuex', 'REST APIs', 'JavaScript', 'Bootstrap'],
  description: 'A comprehensive gym management platform designed to streamline membership management, workout tracking, and trainer coordination through an intuitive and responsive interface.',
  features: [
    'Developed member registration and subscription management with automated plan tracking and renewal status updates',
    'Built workout and diet plan modules allowing trainers to assign and monitor personalized fitness programs',
    'Implemented attendance tracking, payment history management, and role-based dashboards for Admin, Trainer, and Members',
    'Integrated REST APIs for real-time data synchronization between frontend and backend systems',
    'Ensured fully responsive UI design for seamless experience across desktop and mobile devices'
  ]
}

      ]
    }
  }
}
</script>

<style scoped>
.projects {
  padding: 13px 28px;
  margin: 30px;
  background: #f9f9f9;
}

.projects h2 {
  text-align: center;
  font-size: 42px;
  margin-bottom: 10px;
}

.project-card {
  display: flex;
  gap: 40px;
  align-items: center;
  background: white;
  padding: 40px;
  margin-bottom: 40px;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  transition: transform 0.3s, box-shadow 0.3s;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 40px;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 30px rgba(0,0,0,0.12);
}

.project-card.reverse {
  flex-direction: row-reverse;
}

.project-image {
  flex: 1;
  min-width: 300px;
  height: 280px;
  object-fit: cover;
  border-radius: 10px;
}

.project-info {
  flex: 1.2;
}

.project-info h3 {
  font-size: 28px;
  margin-bottom: 15px;
  color: #222;
}

.tech-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 15px;
}

.tech-tag {
  background: #e0e7ff;
  color: #6366f1;
  padding: 5px 12px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: 600;
}

.project-info p {
  color: #666;
  margin-bottom: 12px;
  line-height: 1.8;
}

.project-info ul {
  margin-left: 20px;
  margin-bottom: 20px;
  color: #555;
}

.project-info li {
  margin-bottom: 8px;
}
</style>