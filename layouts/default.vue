<template>
  <div class="app">
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header'
import Footer from '~/components/Footer'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Ubuntu&display=swap');

html,
body {
  margin: 0;
  padding: 0;

  font-family: 'Ubuntu', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

*,
*:before,
*:after {
  box-sizing: border-box;
}

body,
.app {
  min-height: 100vh;

  display: flex;
  flex-direction: column;
  align-items: stretch;

  background: #f3f3f3;

  & > * {
    flex: 1;
  }

  & > header,
  & > footer {
    flex: 0;
  }
}

.container {
  display: block;

  width: 100%;
  max-width: 1000px;

  padding: 15px 20px;
  margin: 0 auto;
}

.btn.branded {
  display: inline-block;
  padding: 0.7em 1.5em;

  cursor: pointer;
  user-select: none;

  box-shadow: 0 5px 20px rgba(0,0,0,0.1), 0 6px 6px rgba(0,0,0,0.1);
  transform: translateY(0);
  cursor: pointer;

  transition: all 0.13s ease-out;

  &:hover {
    box-shadow: 0 10px 20px rgba(0,0,0,0.15), 0 6px 6px rgba(0,0,0,0.15);
    transform: translateY(-3px);
  }

  background: #e01a3f;
  color: white;
  font-size: 1.1em;
}
</style>
