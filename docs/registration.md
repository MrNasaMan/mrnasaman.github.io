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
        title: 'Patient Registration!',
        description: 'Explore this example with an embedded YouTube video.',
        videoSrc: 'https://www.youtube.com/embed/IHMQa_cmNJc?si=Mb4f5DMUJ37hoIOt', // Replace with your video URL
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
    max-width: 800px;
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
    height: 400px;
    border: none;
    border-radius: 10px;
  }
</style>
