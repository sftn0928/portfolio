<template>
  <div class="top-wrapper">
    <div class="hide-block"></div>
    <nuxt-link to="/about">
      <a class="download item"></a>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ishide: true,
      text: "Wellcome to Yosuke's portfolio"
    };
  }
};
</script>

<style scoped>


@keyframes text-in {
  0% {
    transform: translate(0, -100px);
    opacity: 0;
  }
}

.hide-block {
  visibility: hidden;
  margin: 550px 0;
}

.item {
  animation: text-in 0.8s cubic-bezier(0.22, 0.15, 0.25, 1.43) 0s backwards;
}

body {
  margin: 0;
  padding: 0;
  background: #2d2f33;
  font-family: "Varela Round", "Ionicons";
}
::selection {
  background: #3f8efc;
  color: #fff;
}
a {
  text-decoration: none;
}

.download {
  position: absolute;
  top: calc(35% - 30px);
  right: calc(50% - 115px);
  width: 230px;
  height: 60px;
  background-image: -webkit-linear-gradient(
    bottom,
    rgba(0, 0, 0, 0.075),
    rgba(255, 255, 255, 0.045)
  );
  background-image: linear-gradient(
    to top,
    rgba(0, 0, 0, 0.075),
    rgba(255, 255, 255, 0.045)
  );
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.09),
    inset 0 1px 0 rgba(255, 255, 255, 0.04), 0 0 1px rgba(0, 0, 0, 0.3),
    0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 100px;
  color: rgba(255, 255, 255, 0.9);
  line-height: 60px;
  text-align: center;
  letter-spacing: 5px;
  overflow: hidden;
  transition: all 0.3s cubic-bezier(0.67, 0.13, 0.1, 0.81),
    transform 0.15s cubic-bezier(0.67, 0.13, 0.1, 0.81);
}
.download:hover {
  right: calc(50% - 200px);
  width: 400px;
}
.download:active {
  transform: translateY(3px);
}
.download:before,
.download:after {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  opacity: 1;
  transition: all 0.3s cubic-bezier(0.67, 0.13, 0.1, 0.81);
}
.download:before {
  content: "Click to GO! ";
}
.download:after {
  content: "Wellcome to Yosuke's portfolio";
  top: -60px;
  opacity: 0;
}
.download:hover:after {
  top: 0px;
  opacity: 1;
}
.download:hover:before {
  top: 60px;
  opacity: 0;
}
</style>
