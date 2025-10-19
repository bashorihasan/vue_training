<template>
  <section id="team" class="team">
    <div class="container">
      <div class="section-header">
        <h2>Our Team</h2>
        <p>Meet the talented people behind our success</p>
      </div>
      <div class="team-grid">
        <div class="team-member" v-for="member in teamMembers" :key="member.id">
          <div class="member-photo">
            <div class="photo-placeholder">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
          </div>
          <div class="member-info">
            <h3>{{ member.name }}</h3>
            <p class="role">{{ member.role }}</p>
            <p class="description">{{ member.description }}</p>
            <div class="social-links">
              <a href="#" class="social-link">
                <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                </svg>
              </a>
              <a href="#" class="social-link">
                <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                </svg>
              </a>
              <a href="#" class="social-link">
                <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Team',
  data() {
    return {
      teamMembers: [
        {
          id: 1,
          name: 'John Anderson',
          role: 'CEO & Founder',
          description: 'Visionary leader with 15+ years in tech industry'
        },
        {
          id: 2,
          name: 'Sarah Mitchell',
          role: 'CTO',
          description: 'Technology expert passionate about innovation'
        },
        {
          id: 3,
          name: 'Michael Chen',
          role: 'Lead Developer',
          description: 'Full-stack developer with expertise in modern frameworks'
        },
        {
          id: 4,
          name: 'Emily Rodriguez',
          role: 'UI/UX Designer',
          description: 'Creative designer focused on user experiences'
        }
      ]
    }
  }
}
</script>

<style scoped>
.team {
  background: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.section-header {
  text-align: center;
  margin-bottom: 60px;
}

.section-header h2 {
  font-size: 2.5em;
  color: #2c3e50;
  margin-bottom: 10px;
}

.section-header p {
  color: #7f8c8d;
  font-size: 1.1em;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
}

.team-member {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.team-member:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}

.member-photo {
  width: 100%;
  height: 250px;
  overflow: hidden;
}

.photo-placeholder {
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease;
}

.team-member:hover .photo-placeholder {
  transform: scale(1.1);
}

.photo-placeholder svg {
  width: 100px;
  height: 100px;
  color: white;
  opacity: 0.7;
}

.member-info {
  padding: 25px;
  text-align: center;
}

.member-info h3 {
  font-size: 1.4em;
  color: #2c3e50;
  margin-bottom: 5px;
}

.role {
  color: #667eea;
  font-weight: 600;
  margin-bottom: 10px;
  font-size: 0.95em;
}

.description {
  color: #7f8c8d;
  font-size: 0.9em;
  line-height: 1.5;
  margin-bottom: 15px;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 15px;
}

.social-link {
  width: 35px;
  height: 35px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #f8f9fa;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.social-link svg {
  width: 18px;
  height: 18px;
  color: #7f8c8d;
}

.social-link:hover {
  background: #667eea;
}

.social-link:hover svg {
  color: white;
}

@media (max-width: 768px) {
  .team-grid {
    grid-template-columns: 1fr;
  }

  .section-header h2 {
    font-size: 2em;
  }
}
</style>
