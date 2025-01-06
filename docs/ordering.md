<div id="documentation" class="doc-container">
  <div class="section">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
  </div>

  <div class="video-section">
    <h3></h3>
    <iframe 
  :src="videoSrc" 
  title="YouTube video player" 
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen
  class="video-frame">
</iframe>
  </div>
</div>

<script>
  const docApp = {
    data() {
      return {
        title: 'Adding a test with Organization Pay!',
        description: 'Explore this example with an embedded YouTube video.',
        videoSrc: 'https://www.youtube.com/embed/pJbLsh8uSaE?si=mmGoMGOf0V6zvIbj?autoplay=1&controls=1&modestbranding=1&rel=0&iv_load_policy=3&fs=1', // Replace with your video URL
      };
    },
  };

  Vue.createApp(docApp).mount('#documentation');
</script>

<style>
  .doc-container {
    font-family: Arial, sans-serif;
    margin: 20px auto;
    padding: 20px;
    max-width: 1600px;
    border: 1px solid #ccc;
    border-radius: 10px;
    background-color: #fdfdfd;
  }

  .section {
    text-align: center;
    margin-bottom: 20px;
  }

  .section h2 {
    color: #007bff;
    font-size: 2rem;
  }

  .section p {
    font-size: 1.2rem;
    color: #555;
  }

  .video-section {
    text-align: center;
    margin-top: 20px;
  }

  .video-section h3 {
    font-size: 1.5rem;
    color: #007bff;
    margin-bottom: 10px;
  }

  .video-frame {
    width: 100%;
    height: 800px;
    border: none;
    border-radius: 10px;
  }
</style>

