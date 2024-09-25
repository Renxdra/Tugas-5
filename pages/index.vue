<template>
  <div class="container">
    <header class="header">
      <h1>Portofolio</h1>
      <p class="name">Annahl Narendra Wibowo</p>
      <p class="description">Web Developer & Designer</p>
    </header>

    <section class="about">
      <h2>Tentang Saya</h2>
      <div class="profile">
        <img src="https://i.ibb.co.com/bvWGDq9/unnamed.jpg" alt="Profil Annahl Narendra Wibowo" class="profile-image" />
        <p>Saya adalah seorang programmer dengan dalam membangun aplikasi responsif menggunakan teknologi modern. Saya suka tantangan dan selalu berusaha untuk belajar hal baru.</p>
      </div>
    </section>

    <section class="skills">
      <h2>Keahlian</h2>
      <ul>
        <li>HTML, CSS, JavaScript</li>
        <li>Vue.js, Nuxt.js</li>
        <li>Responsive Design</li>
        <li>UI/UX Design</li>
      </ul>
    </section>

    <section class="education">
      <h2>Pendidikan</h2>
      <ul>
        <li>SMAN 1 Maospati</li>
        <li>Vokasi Teknologi Informasi Universitas Brawijaya 2023 - Sekarang</li>
      </ul>
    </section>

    <section class="projects">
      <h2>Proyek Saya</h2>
      <div class="project-list">
        <div class="project" v-for="project in projects" :key="project.id">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" target="_blank">Lihat Proyek</a>
        </div>
      </div>
    </section>

    <footer class="footer">
      <h2>Hubungi Saya</h2>
      <p>Email: <a href="mailto:rendrar179@gmai.com">rendrar179@gmail.com</a></p>
      <div class="social-links">
        <a href="https://github.com/Renxdra" target="_blank" class="social-icon github">GitHub</a>
        <a href="https://www.instagram.com/yourusername" target="_blank" class="social-icon instagram">Instagram</a>
        <a href="https://www.linkedin.com/in/yourusername" target="_blank" class="social-icon linkedin">LinkedIn</a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'website booking sewa kamera',
          description: 'Sebuah website yang dimana untuk menyewakan sebuah kamera untuk kebutuhan dokumentasi',
          link: 'https://desainkamera.vercel.app/',
        },
        {
          id: 2,
          title: 'Redesain sebuah website streaming',
          description: 'Saya redesain ulang sebuah website streaming anime',
          link: 'https://www.figma.com/design/tZcgSknnxbHhyGpEbGAPN9/Annahl-Narendra-Wibowo?node-id=0-1&node-type=canvas&t=P5ye8sy4OYFerlMV-0',
        },
        {
          id: 3,
          title: 'Redesain UI game',
          description: 'Saya meredesain UI COD Warzone',
          link: 'https://www.figma.com/design/j8StWukN92OZNNmgPJ4y27/warzone-Annahl-Narendra-Wibowo?t=P5ye8sy4OYFerlMV-0',
        },
      ],
    };
  },
};
</script>

<style scoped>

body {
  font-family: 'Arial', sans-serif;
  background: linear-gradient(135deg, #e0f7fa 0%, #80deea 100%); /* Latar belakang gradien yang halus */
  color: #333;
  line-height: 1.6;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 900px;
  margin: 20px auto;
  padding: 20px;
  background-color: rgba(255, 255, 255, 0.9); 
  border-radius: 15px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  animation: fadeIn 0.5s ease-in-out;
}


.header {
  text-align: center;
  margin-bottom: 40px;
  background: linear-gradient(135deg, #6ab0f3 0%, #3a79d8 100%);
  color: white;
  padding: 40px 20px;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.header h1 {
  font-size: 2.5rem;
  margin: 0;
}

.name {
  font-size: 2rem;
  font-weight: bold;
  margin: 10px 0;
}

.description {
  font-size: 1.2rem;
}

.about {
  margin-bottom: 40px;
}

.about h2 {
  font-size: 2rem;
  border-bottom: 2px solid #4a90e2;
  padding-bottom: 10px;
  margin-bottom: 20px;
  position: relative;
}

.about h2::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 50px;
  height: 4px;
  background-color: #4a90e2;
}

.profile {
  display: flex;
  align-items: center;
  background-color: #e8f6ff;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.profile-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-right: 20px;
  border: 3px solid #4a90e2;
}

.skills {
  margin-bottom: 40px;
}

.skills h2 {
  font-size: 2rem;
  border-bottom: 2px solid #4a90e2;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.skills ul {
  list-style-type: none;
  padding: 0;
}

.skills li {
  background-color: #cce4ff;
  margin: 5px 0;
  padding: 15px;
  border-radius: 8px;
  position: relative;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.skills li:hover {
  background-color: #99c2ff;
  transform: translateY(-3px);
}

.education {
  margin-bottom: 40px;
}

.education h2 {
  font-size: 2rem;
  border-bottom: 2px solid #4a90e2;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.education ul {
  list-style-type: none;
  padding: 0;
}

.education li {
  background-color: #cce4ff;
  margin: 5px 0;
  padding: 15px;
  border-radius: 8px;
}

.projects {
  margin-bottom: 40px;
}

.projects h2 {
  font-size: 2rem;
  border-bottom: 2px solid #4a90e2;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.project-list {
  display: flex;
  flex-direction: column;
}

.project {
  margin: 10px 0;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
  transition: background-color 0.3s, transform 0.3s;
  position: relative;
}

.project:hover {
  background-color: #e7f3fe;
  transform: translateY(-5px);
}

.project h3 {
  margin: 0;
  font-size: 1.5rem;
  color: #333;
}

.project p {
  margin: 10px 0;
  font-size: 1rem;
}

.project a {
  text-decoration: none;
  color: #4a90e2;
  font-weight: bold;
}

.project a:hover {
  text-decoration: underline;
}

.footer {
  text-align: center;
  margin-top: 40px;
}

.footer h2 {
  font-size: 1.5rem;
  color: #4a90e2;
}

.footer p {
  font-size: 1rem;
}

.social-links {
  margin-top: 15px;
}

.social-icon {
  display: inline-block;
  margin: 0 10px;
  padding: 10px 15px;
  background-color: #4a90e2;
  color: white;
  border-radius: 5px;
  text-decoration: none;
  transition: background-color 0.3s, transform 0.3s;
}

.social-icon:hover {
  background-color: #3a79d8;
  transform: translateY(-2px);
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
