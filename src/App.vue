<template>
  <div class="container">
    <div class="phonePosition">
      <img src="./assets/phone.png" alt="iphoneX" class="phoneFrame">
      <iframe src="http://192.168.0.105:8080/" frameborder="0"></iframe>
    </div>
    <div id="app">
      <div>
        <button @click="selectedComponent ='Profile'">Profile</button>
        <button @click="selectedComponent ='Project'">Project</button>
      </div>
      <keep-alive>
        <component :is="selectedComponent">
          <p>Default render</p>
        </component>
      </keep-alive>
    </div>
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";
import Project from "./components/Project.vue";

export default {
  name: "app",
  components: {
    Profile,
    Project
  },
  data() {
    return {
      selectedComponent: "Profile"
    };
  }
};
</script>

<style>
html {
  height: 100vh;
  box-sizing: border-box;
  background-image: url("assets/bg.jpg");
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
  scroll-behavior: smooth;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

body {
  padding: 0;
  margin: 0;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* disabled pull down refresh */
  overscroll-behavior: contain;
}

.container {
  position: relative;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: rgba(255, 255, 255, 0);
  width: 0;
  position: absolute;
  left: 50%;
  transform: translate(-50%, 50%);
  overflow: hidden;
}

.phoneFrame {
  width: 33rem;
  position: absolute;
  left: 50%;
  transform: translate(-61%, 12%);
}

button {
  padding: 1rem;
  width: 50%;
  border-style: none;
  color: rgb(7, 7, 7);
  background-color: #fff;
  outline: none;
  font-size: 0.9rem;
  border: rgba(218, 218, 218, 0.719) 1px solid;
  border-top: none;
}

button:active {
  -moz-box-shadow: inset 0 0 2px #000000;
  -webkit-box-shadow: inset 0 0 2px #000000;
  box-shadow: inset 0 0 2px #000000;
  transition: all 0.3s;
}

.phonePosition {
  position: relative;
}

iframe {
  overflow: hidden;
  position: absolute;
  width: 313px;
  height: 658px;
  border-style: none;
  transform: translate(-49%, 29.7%);
}

@media only screen and (max-width: 600px) {
  html {
    background-image: none;
    background-color: rgba(169, 255, 188, 0);
  }
  #app {
    width: 100vw;
    transform: translate(-50%, 0%);
    overflow: visible;
  }
  .phoneFrame {
    width: 0;
  }
  iframe {
    display: none;
  }
}
</style>
