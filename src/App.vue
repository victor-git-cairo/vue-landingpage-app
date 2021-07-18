<template>
  <div id="app">
    <nav-bar></nav-bar>

    <div class="hero-box">
      <div class="hero-box-left">
        <p class="large-text">
          Your trusted web developers, just a click away.
        </p>
        <p class="medium-text">
          Meet our team of web dev experts ready to take on your biggest
          challenges and turn them into opportunities to outshine your
          competition. Connect with us today to get started.
        </p>
      </div>
    <forms />

    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Forms from "./components/Forms";


export default {
  name: "App",
  components: {
    NavBar,
  
    Forms,
  },

  data() {
    return {
      nav: [
        { title: "Home", link: "#home" },
        {
          title: "About",
          link: "#about",
          subLinks: [
            { title: "History", link: "#history" },
            { title: "Our Team", link: "#team" },
          ],
          subLinkModal: false,
        },
        {
          title: "Services",
          link: "#services",
          subLinks: [
            { title: "Audio", link: "#audio" },
            { title: "Video", link: "#video" },
            { title: "Web", link: "#web" },
          ],
          subLinkModal: false,
        },
      ],
    };
  },

  methods: {
    toggleSubModal: function (item) {
      if (item.subLinks) {
        item.subLinkModal = !item.subLinkModal;
      }
    },
  },
};
</script>

<style>
body {
  background: #fff;
  color: #777;
}
.logo {
  color: #3d3d3d;
  display: flex;
}
.nav-wrapper {
  background: #ffffff;
  display: flex;
  justify-content: space-between;
  padding: 15px 25px;
}
.link-item {
  color: #555ae4;
  font-weight: bold;
  font-size: 14px;
  padding: 5px 10px;
  border-radius: 5px;
  margin-left: 5px;
  position: relative;
}
.link-item:active,
.link-item:hover,
.link-active {
  background: #555ae4;
  color: #fff;
}
.sublinks {
  position: absolute;
  top: 40px;
  right: 10px;
  align-items: flex-end;
  display: flex;
  flex-direction: column;
  background: #3d3d3d;
  padding: 10px;
  border-radius: 5px;
}
.sublinks > a {
  color: #eee;
  width: 100px;
}
.hero-box {
  background: #f3f3ff;
  display: flex;
}
.hero-box-left {
  width: 400px;
  margin: 25px;
}
.hero-box-right {
  width: 100%;
  margin: 25px;
}
.large-text {
  font-size: 25px;
  line-height: 1.5em;
}
.medium-text {
  margin-top: 10px;
}
.input-wrapper {
  display: flex;
  flex-direction: column;
  margin-bottom: 15px;
}
.input-wrapper > label {
  font-size: 14px;
  font-weight: bold;
  margin-bottom: 5px;
}
.input-wrapper > input {
  background: transparent;
  border: 1px solid #555ae4;
  border-radius: 5px;
  padding: 5px;
}
.input-wrapper > button {
  background: #555ae4;
  color: #fff;
  border-radius: 5px;
  padding: 10px;
}
</style>
