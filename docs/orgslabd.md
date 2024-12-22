
<div id="documentation" class="doc-container">
  <div class="section">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
    <img :src="imageSrc" :alt="imageAlt" class="doc-image" />
  </div>

  <div class="interactive-section">
    <h3>Interactive Example</h3>
    <p>{{ interactiveText }}</p>
    <button class="btn" @click="toggleText">{{ buttonText }}</button>
  </div>
</div>

<script>
  const docApp = {
    data() {
      return {
        title: 'Welcome to Vue Documentation!',
        description: 'This is a simple Vue template for showcasing documentation with text and images.',
        imageSrc: 'https://via.placeholder.com/400x200.png?text=Docsify+Image',
        imageAlt: 'Placeholder Image',
        interactiveText: 'Click the button below to toggle this text!',
        buttonText: 'Toggle Text',
        isTextVisible: true,
      };
    },
    methods: {
      toggleText() {
        this.isTextVisible = !this.isTextVisible;
        this.interactiveText = this.isTextVisible
          ? 'Click the button below to toggle this text!'
          : 'You toggled the text!';
      },
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
    color: #42b983;
    font-size: 2rem;
  }

  .section p {
    font-size: 1.2rem;
    color: #555;
  }

  .doc-image {
    max-width: 100%;
    height: auto;
    margin: 15px 0;
    border-radius: 10px;
  }

  .interactive-section {
    text-align: center;
    margin-top: 20px;
  }

  .btn {
    padding: 10px 20px;
    font-size: 1rem;
    color: #fff;
    background-color: #42b983;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .btn:hover {
    background-color: #369f6e;
  }
</style>