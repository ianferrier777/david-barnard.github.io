<script setup lang="ts">
import * as loremIpsum from './data/loremIpsum'
</script>

<template>
  <div class="app-container">
    <nav class="navigation">
      <a>Home</a>
      <a class="topbar-logo-wrapper">
        <img class="topbar-logo" src="./assets/logoPlaceholder.png" />
      </a>
      <a>About</a>
    </nav>

    <div class="video-section">
      <video autoplay muted loop>
        <source src="./assets/rickRoll.mp4" type="video/mp4" />
        There was an issue loading the video.
      </video>
    </div>

    <div class="container">
      <div class="columns">
        <div class="column">
          <img src="./assets/david1.png" alt="David" class="image-content" />
          <div class="cta-section">
            <h2>Call to Action</h2>
            <ul>
              <li>Volunteer: www.signyourlifeaway.com</li>
              <li>Join our community: www.thisisyourlifenow.com</li>
            </ul>
            <h2>Contact</h2>
            <p>Contact us at info@example.com</p>
          </div>
        </div>
        <div class="column">
          <img src="./assets/projectPlaceholder.png" alt="Upcoming Project" class="project-image" />
          <div class="project-description">
            <h2>Upcoming Project</h2>
            <p>
              Lorem ipsum odor amet, consectetuer adipiscing elit. Nisi ultrices felis nullam nisi;
              integer rhoncus ridiculus. Varius habitant netus pulvinar hendrerit semper platea
              euismod purus. Gravida dignissim suscipit vivamus; placerat bibendum rhoncus vulputate
              aptent. Dis nibh mus phasellus ipsum placerat. Facilisis litora etiam pulvinar nostra
              integer curabitur nullam. Blandit facilisis augue urna ornare adipiscing. Hac taciti
              torquent dolor magna condimentum. Justo potenti habitasse tortor condimentum maecenas
              congue velit duis.
            </p>
          </div>
          <div class="upcoming-shows">
            <h2>Upcoming Shows</h2>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
            <p>Show - Date & Venue</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.app-container {
  margin: 32px;
  background-color: rgba(250, 243, 229, 0.6);
  border-radius: 50px;
}
.container {
  padding-top: 16px;
  padding-bottom: 16px;
  padding-right: 32px;
  padding-left: 32px;
  box-sizing: border-box; /* Ensure padding is included in total width/height */
}

.navigation {
  height: 60px; /* Adjust height as needed */
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  background: rgba(255, 255, 255, 0.7); /* Semi-transparent white */
  backdrop-filter: blur(10px); /* Glossy effect */
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1000; /* Ensure it stays above other content */
  width: 100%;
  border-radius: 5px;
  gap: 32px;
}

.topbar-logo-wrapper {
  display: flex;
  justify-content: center;
  /* width: 10%; */
}

.topbar-logo {
  /* width: 10%; */
  width: 20%;
  border-radius: 20px;
}

.video-section {
  width: 100vw;
  margin: -32px;
  height: calc(100vh - 60px - 200px); /* Deduct height of topbar and bottom sections */
  overflow: hidden;
  padding-top: 60px;
}

.video-section video {
  width: 100vw;
  height: 100%;
  object-fit: cover;
}

.columns {
  display: flex;
  gap: 32px;
}

.column {
  display: flex;
  flex-direction: column;
  gap: 16px;
  width: 50%;
  padding: 32px;
}

.image-content {
  border-top-left-radius: 8px;
  border-top-right-radius: 40px;
  border-bottom-left-radius: 40px;
  border-bottom-right-radius: 8px;
  width: 100%;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
}

.cta-section {
  border-top-left-radius: 50px;
  border-top-right-radius: 100px;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  padding: 16px;
  background-color: rgba(236, 250, 229, 0.7);
  /* border-radius: 5px; */
  box-shadow: -1px 5px 2.5px rgba(0, 0, 0, 0.02);
}

.project-image {
  width: 50%;
  border-radius: 40px;
}

.project-description {
  border-top-left-radius: 125px;
  border-top-right-radius: 50px;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  text-align: right;
  margin-left: 25%;
  padding: 16px;
  background-color: rgba(236, 250, 229, 0.7);
  box-shadow: 3px -3px 2.5px rgba(0, 0, 0, 0.02);
}

.upcoming-shows {
  border-top-left-radius: 150px;
  border-top-right-radius: 50px;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  text-align: right;
  padding: 16px;
  background-color: rgba(236, 250, 229, 0.7);
  width: 60%;
  margin-left: 10%;
  box-shadow: 5px 5px 2.5px rgba(0, 0, 0, 0.02);
}
</style>
