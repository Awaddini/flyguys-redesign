<template>
  <div id="app">

    <app-header></app-header>
    <app-content></app-content>

  </div>
</template>

<script>
import Header from './components/shared/Header.vue';
import Content from './components/Content.vue';
export default {
  
  data () {
    return {
      
    }
  },
  components: {
    'app-header': Header,
    'app-content': Content
  }
}
</script>

<style lang="scss">

$primary-color: #FE4B57;
$secondary-color: #A874F6;
$third-color: #2c3e50;


html, body {
  height: 100%;
  margin: 0;
}

#app {
  font-family: 'Open Sans';
	font-weight: 300;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100%;
  // position: relative;
  background-size: cover;
  background: linear-gradient(135deg, #FE4B57, #A874F6);
  color: #fff;

  z-index: 10;
  
  display: grid;
  grid-template-rows: max-content 1fr;
  
}  


#app::before {
  content: ' ';
  width: 100%;
  height: 100%;
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 0;
  background-image: url('./assets/spikes.png');
  background-repeat: no-repeat;
  background-position: center center;
  background-attachment: fixed;

  background-size: cover;

  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

#app > * {
  position: relative;
  cursor: default;
}



button {
  border-radius: 2px;
  padding: 3px 16px;
  box-sizing: border-box;
  border: 1px solid #fff;
  background: 0;
  color: #fff;
}


h1, h2, p {
  font-weight: normal;
}

p {
  font-size: 0.85rem;
}

a {
  color: $third-color;
}


.brand {
  justify-self: start;
  font-size: 1.5rem;
}
</style>
