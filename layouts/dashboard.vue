<template>
  <div class="dashboard">
    <Sidebar />
    <div class="main">
      <nuxt class="container" />
    </div>
  </div>
</template>

<script>
import Sidebar from '~/components/Sidebar'

export default {
  components: {
    Sidebar
  }
}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Ubuntu&display=swap");

html,
body {
  margin: 0;
  padding: 0;
  font-family: "Ubuntu", sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

.dashboard {
  min-height: 100vh;
  display: flex;
  flex-direction: row;
  align-items: stretch;

  background: #f3f3f3;

  & > * {
    flex: 0;
  }

  .main {
    flex: 1;
  }

  table {
    border-collapse: collapse;
    width: 100%;

    td,
    th {
      border: 1px solid black;
      padding: 8px;
      text-align: center;

      a {
        // text-decoration: none;
        color: inherit;
      }
    }

    thead tr {
      background: #264e42;
      color: white;
    }

    tr:nth-child(even) {
      background: white;
    }
  }

  label,
  input:not([type=checkbox]),
  textarea {
    display: block;
    font-size: 1.15em;
    margin: 0.5em 0;
  }

  input:not([type=checkbox]),
  textarea {
    // width: 100%;
    width: 400px;
    max-width: 400px;
    padding: 0.25em 0.5em;
  }

}

.container {
  display: block;
  width: 100%;
  max-width: 1000px;

  padding: 15px 20px;
  margin: 0 auto;
}

.btn.dash {
  display: inline-block;
  padding: 0.7em 1.5em;

  cursor: pointer;
  user-select: none;

  box-shadow: 0 5px 20px rgba(0,0,0,0.1), 0 6px 6px rgba(0,0,0,0.1);
  cursor: pointer;

  background-color: rgba(38, 78, 66, 1);
  color: white;
  font-size: 1.1em;

  &:hover {
    box-shadow: 0 5px 20px rgba(0,0,0,0.15), 0 6px 6px rgba(0,0,0,0.15);
    background: darken($color: #264e42, $amount: 5)
  }
}
</style>
