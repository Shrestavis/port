<template>
  <div class="hello">
    <div class="container">
      <nav>
        <span>Work</span>
        <span>Contact</span>
      </nav>
      <section class="hero">
        <div class="wrapper">
          <div class="hero-wrapper">
            <div class="hero-content">
              <h1 class="hero-title">Hello</h1>
              <p class="hero-text">
                My name is Siva Krishna and I love to create beautiful pixels.
                <br> I'm a Indian Experince Design freelancer, currently working at
                <br> Broadridge
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'hello',
    data() {
      return {
        msg: 'Welcome to Your Vue.js PWA'
      }
    }
  }
</script>
<style type="text/css">
  html,
  body {
    overflow: auto;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    background: #453f52;
    height: 100%;
  }

  nav {
    padding: 10px;
    margin: 10px;
    position: absolute;
    top: 60px;
    color: #eee;
    z-index: 999;
  }

  nav span {
    padding: 10px;
    margin: 10px;
    cursor: pointer
  }

  nav span:hover {
    border-bottom: 2px solid #8947ff
  }

  * {
    outline: none;
    transition: all .35s ease-in-out
  }

  a {
    text-decoration: none;
    color: inherit;
  }

  #app {
    position: absolute;
    height: 100%;
    width: 100%;
  }

  section {
    display: block;
  }

  button {
    padding: 15px 35px;
    cursor: pointer;
    background: inherit;
    border: inherit;
    color: inherit;
    border-radius: 25px;
    font-size: 18px;
    margin: 10px;
  }

  .hero,
  .features,
  .feedback,
  .preview,
  .conclusion {
    position: relative;
  }

  .feedback {
    height: 300px;
    text-align: center;
    color: #eee;
    font-size: 170%;
    line-height: 2;
  }

  .preview {
    text-align: center;
    background-color: #eee;
  }

  .preview img {
    height: 300px;
    margin: 10px;
  }

  .wrapper {
    width: 1000px;
    margin: 0 auto;
  }

  .hero {
    padding: 0 40px;
  }

  .hero-wrapper {
    height: 100vh;
    min-height: 600px;
    padding: 40px 0;
    box-sizing: border-box;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .hero-title,
  .pre-title,
  .fea-title {
    font-weight: 100;
    font-size: 40px;
    line-height: 1.5;
    left: 0;
  }

  .pre-title,
  .fea-title {
    color: #333;
  }

  .hero-title::after {
    content: "";
    display: block;
    line-height: 1em;
    border-bottom: 8px solid #8947ff;
    width: 40px;
  }

  .hero-content {
    max-width: 450px;
    font-size: 18px;
    line-height: 2;
    color: #eee;
  }

  .hero-text {
    height: 75px;
  }

  .primary {
    background: #27ae60;
  }

  .secondary {
    border: 1px solid #27ae60;
  }

  .prev-img {
    transform: scale(1.2);
  }

  @media only screen and (max-width: 480px) {
    .wrapper {
      width: 100%;
      margin: 0 auto;
    }
    .prev-img {
      width: 300px;
    }
    .action-buttons {
      text-align: center;
    }
    .hero-wrapper {
      /* flex-direction: column-reverse; */
      height: auto;
      min-height: auto;
      padding-top: 80px;
    }
  }
</style>
