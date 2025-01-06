<div id="introduction" class="intro-container">
  <div class="intro-image">
    <img src="/_media/GLS.png" alt="Introduction Image" />
  </div>
  <h1>{{ title }}</h1>
  <p>{{ subtitle }}</p>

  <div class="features">
    <h2>Topics</h2>
    <ul>
      <li v-for="feature in features" :key="feature">{{ feature }}</li>
    </ul>
  </div>

  <div class="get-started">
    <h2>Get Started</h2>
    <p>Use the navigation menu on the left to explore the sections. Start with:</p>
    <ul>
      <li><a href="#/registration">Patient Registration</a></li>
      <li><a href="#/ordering">Adding a Test (Org Pay)</a></li>
      <li><a href="#/orderingins">Adding a Test (Insurance)</a></li>
    </ul>
  </div>
</div>

<script>
  const introApp = {
    data() {
      return {
        title: 'Welcome to Genics Laboratory System (GLS) Documentation',
        subtitle: 'Your guide to mastering GLS with clear examples and explanations.',
        features: [
          'Learn how to register a patient',
          'Learn how to order a test',
          'Retrieve Results',
        ],
      };
    },
  };

  Vue.createApp(introApp).mount('#introduction');
</script>

<style>
  /* Container Styling */
  .intro-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 30px;
    background-color: #ffffff;
    border-radius: 15px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    font-family: 'Roboto', sans-serif;
    text-align: center;
  }

  /* Title Styling */
  .intro-container h1 {
    font-size: 3rem;
    font-weight: 700;
    color: #2d3a55;
    margin-bottom: 15px;
  }

  /* Subtitle Styling */
  .intro-container p {
    font-size: 1.2rem;
    color: #666;
    margin-bottom: 30px;
    line-height: 1.6;
  }

  /* Features Section */
  .features {
    text-align: left;
    margin-top: 40px;
  }

  .features h2 {
    font-size: 2rem;
    color: #2d3a55;
    font-weight: 600;
    margin-bottom: 15px;
  }

  .features ul {
    list-style: none;
    padding-left: 0;
    font-size: 1.1rem;
    color: #555;
  }

  .features ul li {
    margin-bottom: 15px;
    padding-left: 25px;
    position: relative;
  }

  .features ul li:before {
    content: '✔';
    color: #3d8ef7;
    position: absolute;
    left: 0;
    top: 0;
  }

  /* Get Started Section */
  .get-started {
    text-align: left;
    margin-top: 40px;
  }

  .get-started h2 {
    font-size: 2rem;
    color: #2d3a55;
    font-weight: 600;
    margin-bottom: 15px;
  }

  .get-started ul {
    list-style: none;
    padding-left: 0;
    font-size: 1.1rem;
  }

  .get-started ul li {
    margin-bottom: 15px;
  }

  .get-started ul li a {
    color: #3d8ef7;
    text-decoration: none;
    font-weight: 500;
  }

  .get-started ul li a:hover {
    text-decoration: underline;
  }

  /* Button Styling */
  .cta-button {
    display: inline-block;
    padding: 15px 30px;
    background-color: #3d8ef7;
    color: white;
    font-size: 1.2rem;
    border-radius: 30px;
    text-decoration: none;
    margin-top: 30px;
    transition: background-color 0.3s ease;
  }

  .cta-button:hover {
    background-color: #1c6eff;
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .intro-container {
      padding: 20px;
    }

    .intro-container h1 {
      font-size: 2.5rem;
    }

    .features h2, .get-started h2 {
      font-size: 1.8rem;
    }

    .features ul li, .get-started ul li {
      font-size: 1rem;
    }
  }
</style>
