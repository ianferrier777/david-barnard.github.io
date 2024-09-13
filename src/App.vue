<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div id="app">
    <nav class="topbar">
      <router-link to="/" class="nav-link">Home</router-link>
      <img src="./assets/logoPlaceholder.png" alt="Site Logo" class="site-logo" />
      <router-link to="/about" class="nav-link">About</router-link>
    </nav>

    <router-view />

    <div class="main-content">
      <div class="video-section">
        <video controls>
          <source src="./assets/logoPlaceholder.png.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>

      <div class="content-columns">
        <!-- Left Column -->
        <div class="left-column">
          <img src="./assets/david1.png" alt="Image" class="image-content" />
          <div class="cta-section">
            <h3>Call to Action</h3>
            <p>Contact us at info@example.com</p>
          </div>
        </div>

        <!-- Right Column -->
        <div class="right-column">
          <img src="./assets/projectPlaceholder.png" alt="Upcoming Project" class="project-image" />
          <div class="project-description">
            <h3>Upcoming Project</h3>
            <p>Description of the upcoming project...</p>
          </div>
          <div class="upcoming-shows">
            <h3>Upcoming Shows</h3>
            <ul>
              <li>Show 1 - Date & Venue</li>
              <li>Show 2 - Date & Venue</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Background for old paper */
#app {
  background-color: #f4ecd8;
  background-image: url('/path-to-old-paper-background.jpg');
  background-size: cover;
  min-height: 100vh;
}

/* Topbar Navigation */
.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #8c6e44;
  padding: 16px;
  height: 80px; /* Set a fixed height for the topbar */
  width: 100%;  /* Ensure it takes up the full width */
  box-sizing: border-box; /* Ensures padding doesn't affect width */
}

.nav-link {
  color: #ffffff;
  text-decoration: none;
  font-size: 18px;
  padding: 0 16px;
}

.site-logo {
  height: 80px;
  margin-top: -16px;
  margin-bottom: -16px;
  object-fit: contain; /* Ensure the logo doesn't stretch */
}

/* Main content area */
.main-content {
  padding: 16px;
}

.video-section {
  padding: 32px;
}

@media (max-width: 680px) {
  .video-section {
    padding: 16px;
  }
}

.content-columns {
  display: flex;
  justify-content: space-between;
}

.left-column, .right-column {
  flex: 1;
  padding: 16px;
}

.image-content {
  width: 100%;
  height: auto;
}

/* Style for Call to Action and Upcoming Projects */
.cta-section, .project-description, .upcoming-shows {
  margin-top: 16px;
}

.upcoming-shows ul {
  list-style: none;
  padding: 0;
}
</style>
