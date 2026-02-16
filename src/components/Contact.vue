<template>
  <section class="contact-section" id="contacts">
    <div class="contact-container">
      <div class="contact-header">
        <h2 data-aos="fade-up">Get In Touch</h2>
        <p class="contact-subtitle" data-aos="fade-up" data-aos-delay="100">Let's work together!</p>
      </div>

      <div class="contact-content">
        <!-- Contact Info Side -->
        <div class="contact-info" data-aos="fade-right" data-aos-delay="200">
          <!-- Illustration Image -->
          <div class="contact-illustration">
            <img src="https://images.unsplash.com/photo-1596526131083-e8c633c948d2?w=600&h=400&fit=crop" alt="Contact Illustration">
          </div>
          <div class="info-card">
            <div class="icon-wrapper">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                <polyline points="22,6 12,13 2,6"></polyline>
              </svg>
            </div>
            <div class="info-content">
              <h3>Email</h3>
              <p>thanalakshmipaulraj@gmail.com</p>
            </div>
          </div>

          <div class="info-card">
            <div class="icon-wrapper">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
                <circle cx="12" cy="10" r="3"></circle>
              </svg>
            </div>
            <div class="info-content">
              <h3>Location</h3>
              <p>Chennai, Tamil Nadu, India</p>
            </div>
          </div>

          <div class="info-card">
            <div class="icon-wrapper">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
              </svg>
            </div>
            <div class="info-content">
              <h3>Phone</h3>
              <p>+91 9025648381</p>
            </div>
          </div>

          <!-- <div class="social-links">
            <a href="https://linkedin.com" target="_blank" class="social-icon linkedin">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
              </svg>
            </a>
            <a href="https://github.com" target="_blank" class="social-icon github">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="https://twitter.com" target="_blank" class="social-icon twitter">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
              </svg>
            </a>
          </div> -->
        </div>

        <!-- Contact Form Side -->
        <div class="contact-form-wrapper" data-aos="fade-left" data-aos-delay="300">
          <form @submit.prevent="sendEmail" class="contact-form">
            <div class="form-group">
              <label for="name">Your Name</label>
              <input 
                type="text" 
                id="name" 
                v-model="formData.name" 
                placeholder="Enter your name"
                :class="{ 'error': errors.name }"
                @input="clearError('name')"
                required
              >
              <span v-if="errors.name" class="error-message">{{ errors.name }}</span>
            </div>

            <div class="form-group">
              <label for="email">Your Email</label>
              <input 
                type="email" 
                id="email" 
                v-model="formData.email" 
                placeholder="Enter your email"
                :class="{ 'error': errors.email }"
                @input="clearError('email')"
                required
              >
              <span v-if="errors.email" class="error-message">{{ errors.email }}</span>
            </div>

            <div class="form-group">
              <label for="subject">Subject</label>
              <input 
                type="text" 
                id="subject" 
                v-model="formData.subject" 
                placeholder="What's this about?"
                :class="{ 'error': errors.subject }"
                @input="clearError('subject')"
                required
              >
              <span v-if="errors.subject" class="error-message">{{ errors.subject }}</span>
            </div>

            <div class="form-group">
              <label for="message">Message</label>
              <textarea 
                id="message" 
                v-model="formData.message" 
                rows="5" 
                placeholder="Tell me about your project..."
                :class="{ 'error': errors.message }"
                @input="clearError('message')"
                required
              ></textarea>
              <span v-if="errors.message" class="error-message">{{ errors.message }}</span>
            </div>

            <button type="submit" class="submit-btn" :disabled="isSubmitting">
              <span v-if="!isSubmitting">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="22" y1="2" x2="11" y2="13"></line>
                  <polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
                </svg>
                Send Message
              </span>
              <span v-else>
                <div class="spinner"></div>
              </span>
            </button>
          </form>

          <!-- Success Message -->
          <transition name="fade">
            <div v-if="showSuccess" class="success-message">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path>
                <polyline points="22 4 12 14.01 9 11.01"></polyline>
              </svg>
              <p>Message sent successfully! I'll get back to you soon.</p>
            </div>
          </transition>

          <!-- Error Message -->
          <transition name="fade">
            <div v-if="showError" class="error-alert">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="12" cy="12" r="10"></circle>
                <line x1="15" y1="9" x2="9" y2="15"></line>
                <line x1="9" y1="9" x2="15" y2="15"></line>
              </svg>
              <p>{{ errorMessage }}</p>
            </div>
          </transition>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import emailjs from '@emailjs/browser'

export default {
  name: 'Contact',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        subject: '',
        message: ''
      },
      errors: {},
      isSubmitting: false,
      showSuccess: false,
      showError: false,
      errorMessage: ''
    }
  },
  methods: {
    validateForm() {
      this.errors = {}
      let isValid = true

      if (!this.formData.name.trim()) {
        this.errors.name = 'Name is required'
        isValid = false
      }

      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
      if (!this.formData.email.trim()) {
        this.errors.email = 'Email is required'
        isValid = false
      } else if (!emailPattern.test(this.formData.email)) {
        this.errors.email = 'Please enter a valid email'
        isValid = false
      }

      if (!this.formData.subject.trim()) {
        this.errors.subject = 'Subject is required'
        isValid = false
      }

      if (!this.formData.message.trim()) {
        this.errors.message = 'Message is required'
        isValid = false
      } else if (this.formData.message.trim().length < 10) {
        this.errors.message = 'Message should be at least 10 characters'
        isValid = false
      }

      return isValid
    },

    clearError(field) {
      if (this.errors[field]) {
        this.$delete(this.errors, field)
      }
    },

    async sendEmail() {
      if (!this.validateForm()) {
        return
      }

      this.isSubmitting = true
      this.showSuccess = false
      this.showError = false

      try {
        // Initialize EmailJS with your public key
        emailjs.init('YOUR_PUBLIC_KEY') // Replace with your EmailJS public key

        // Send email using EmailJS
        const response = await emailjs.send(
          'YOUR_SERVICE_ID',  // Replace with your EmailJS service ID
          'YOUR_TEMPLATE_ID', // Replace with your EmailJS template ID
          {
            from_name: this.formData.name,
            from_email: this.formData.email,
            subject: this.formData.subject,
            message: this.formData.message,
            to_name: 'Thanalakshmi' // Your name
          }
        )

        console.log('Email sent successfully:', response)
        
        // Show success message
        this.showSuccess = true
        
        // Reset form
        this.formData = {
          name: '',
          email: '',
          subject: '',
          message: ''
        }

        // Hide success message after 5 seconds
        setTimeout(() => {
          this.showSuccess = false
        }, 5000)

      } catch (error) {
        console.error('Email send failed:', error)
        this.showError = true
        this.errorMessage = 'Failed to send message. Please try again or email me directly.'
        
        // Hide error message after 5 seconds
        setTimeout(() => {
          this.showError = false
        }, 5000)
      } finally {
        this.isSubmitting = false
      }
    }
  }
}
</script>

<style scoped>
.contact-section {
  padding:20px;
  margin: 30px;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
  position: relative;
  overflow: hidden;
}

.contact-section::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle, rgba(253, 181, 21, 0.1) 0%, transparent 70%);
  border-radius: 50%;
}

.contact-container {
  max-width: 1200px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.contact-header {
  text-align: center;
  margin-bottom: 25px;
}

.contact-header h2 {
  font-size: 48px;
  font-weight: 700;
  color: #222;
  margin-bottom: 15px;
}

.contact-subtitle {
  font-size: 20px;
  color: #666;
  font-weight: 400;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 60px;
  align-items: start;
}

/* Contact Info Side */
.contact-info {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.contact-illustration {
  width: 100%;
  margin-bottom: 10px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
}

.contact-illustration:hover {
  transform: scale(1.02);
}

.contact-illustration img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  display: block;
}

.info-card {
  display: flex;
  align-items: center;
  gap: 20px;
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
}

.info-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12);
}

.icon-wrapper {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #FDB515 0%, #f59e0b 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
}

.info-content h3 {
  font-size: 18px;
  font-weight: 600;
  color: #222;
  margin-bottom: 5px;
}

.info-content p {
  font-size: 15px;
  color: #666;
  margin: 0;
}

.social-links {
  display: flex;
  gap: 15px;
  margin-top: 10px;
}

.social-icon {
  width: 45px;
  height: 45px;
  background: white;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #666;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
}

.social-icon:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.social-icon.linkedin:hover {
  background: #0077b5;
  color: white;
}

.social-icon.github:hover {
  background: #333;
  color: white;
}

.social-icon.twitter:hover {
  background: #1da1f2;
  color: white;
}

/* Contact Form Side */
.contact-form-wrapper {
  background: white;
  padding: 45px;
  border-radius: 16px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.form-group label {
  font-size: 15px;
  font-weight: 600;
  color: #333;
}

.form-group input,
.form-group textarea {
  padding: 14px 18px;
  border: 2px solid #e5e7eb;
  border-radius: 10px;
  font-size: 15px;
  font-family: inherit;
  transition: all 0.3s ease;
  background: #f9fafb;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #FDB515;
  background: white;
  box-shadow: 0 0 0 3px rgba(253, 181, 21, 0.1);
}

.form-group input.error,
.form-group textarea.error {
  border-color: #ef4444;
}

.form-group textarea {
  resize: vertical;
  min-height: 120px;
}

.error-message {
  font-size: 13px;
  color: #ef4444;
  margin-top: -5px;
}

.submit-btn {
  padding: 16px 32px;
  background: linear-gradient(135deg, #FDB515 0%, #f59e0b 100%);
  color: white;
  border: none;
  border-radius: 10px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-top: 10px;
}

.submit-btn:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(253, 181, 21, 0.4);
}

.submit-btn:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.submit-btn svg {
  width: 18px;
  height: 18px;
}

.spinner {
  width: 18px;
  height: 18px;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-top-color: white;
  border-radius: 50%;
  animation: spin 0.8s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* Success and Error Messages */
.success-message,
.error-alert {
  margin-top: 20px;
  padding: 18px 20px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 15px;
  animation: slideIn 0.3s ease;
}

.success-message {
  background: #d1fae5;
  color: #065f46;
  border: 1px solid #6ee7b7;
}

.error-alert {
  background: #fee2e2;
  color: #991b1b;
  border: 1px solid #fca5a5;
}

.success-message svg,
.error-alert svg {
  flex-shrink: 0;
}

.success-message p,
.error-alert p {
  margin: 0;
  font-weight: 500;
}

/* Fade Transition */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive Design */
@media (max-width: 968px) {
  .contact-content {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .contact-header h2 {
    font-size: 38px;
  }

  .contact-form-wrapper {
    padding: 35px;
  }
}

@media (max-width: 640px) {
  .contact-section {
    padding: 60px 20px;
    margin: 20px 10px;
  }

  .contact-header h2 {
    font-size: 32px;
  }

  .contact-subtitle {
    font-size: 16px;
  }

  .contact-form-wrapper {
    padding: 25px;
  }

  .info-card {
    padding: 20px;
  }

  .social-links {
    justify-content: center;
  }
}
</style>