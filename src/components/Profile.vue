<template>
  <div class="hello">
    <img src="https://www.dropbox.com/s/jr83zjdsa0rpj1c/me.png?raw=1" alt="profile picture" class="proPic">
    <h2>你好!</h2>
    <h3>I'm Stephen Chow</h3>
    <h3>Mobile Web Developer</h3>
    <h3>- Vue.js and PWA specialist - </h3>
    <div class="logoVuePWA">
      <img src="../assets/vue.png" alt="vuejs logo" class="logo vueLogo">
      <img src="../assets/pwa.png" alt="pwa logo" class="logo pwaLogo">
    </div>
    <p>reach me through :</p>
    <div class="socialMedia">
      <a href="https://www.github.com/stevchow" target="blank"><i class="fa fa-github"></i></a>
      <a href="https://www.linkedin.com/in/stevchow" target="blank"><i class="fa fa-linkedin"></i></a>
      <a href="https://www.medium.com/@stevchow" target="blank"><i class="fa fa-medium"></i></a>
      <a href="mailto:stephen_chow97@live.com"><i class="fa fa-envelope-o"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  margin-top: 1.3rem;
  color: rgb(56, 41, 41);
  overflow: hidden;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #000000;
}

.logoVuePWA {
  position: relative;
  margin-bottom: 1rem;
}

.proPic {
  border-radius: 5rem;
  filter: brightness(102%);
  width: 6rem;
  margin-bottom: 1rem;
}

.vueLogo {
  position: relative;
  transform: translate(-15%, 15%);
  width: 7rem;
}

.pwaLogo {
  position: relative;
  transform: translate(20%, -20%);
  width: 10rem;
}

.socialMedia {
  font-size: 3rem;
  transform: translateX(6%);
}

.fa {
  margin-right: 2.8rem;
}
.fa:hover {
  color: rgb(63, 150, 248);
}
</style>
