<template>
  <div id="app">
    <home-page></home-page>
    <main class="main">
      <social-media />
      <album></album>
      <contact-info />
      <camera-carrousel />
    </main>
    <footer-page></footer-page>
  </div>
</template>

<script>
import HomePage from './components/home-page/HomePage'
import FooterPage from './components/footer-page/FooterPage'
import Album from './components/album/Album'
import SocialMedia from './components/social-media/SocialMedia'
import CameraCarrousel from './components/camera-carrousel/CameraCarrousel'
import ContactInfo from './components/contact-info/ContactInfo'

export default {
  name: 'App',
  components: {
    HomePage,
    FooterPage,
    Album,
    SocialMedia,
    CameraCarrousel,
    ContactInfo
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300&display=swap');
* {
  font-family: 'Roboto', sans-serif;
}

:root {
  --primary-color: white;
  --secondary-color: #2f2f2f;
  --thirdy-color: #CFB53B;
}

#app {
  width: 100%;
  height: 100%;
  background-color: var(--primary-color);
  display: flex;
  flex-direction: column;
}
body {
  margin: unset;
}

.home-page {
  flex: 1;
  min-height: 100vh;
  max-height: 100vh;
  background-color: var(--secondary-color);
}

.main {
  background-color: var(--primary-color);

  .social-media {
    background-color: var(--secondary-color);
    min-height: 25vh;
  }
}

.footer-page {
  flex: 1;
  min-height: 200px;
  max-height: 300px;
  background-color: var(--secondary-color);
}

</style>
