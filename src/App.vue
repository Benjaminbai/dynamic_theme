<template>
  <div id="app">
    <button @click="clickHandle('red')" class="my-button">
      点击切换全局颜色
    </button>
    <a-button type="primary">antd 的 button</a-button>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import less from "less";
export default {
  name: "App",
  components: {
    HelloWorld,
  },
  methods: {
    clickHandle(color) {
      less
        .modifyVars({ "@primary-color": color })
        .then(() => {
          console.log("切换成功", color);
        })
        .catch(() => {
          console.log("切换失败");
        });
      less.refreshStyles();
    },
  },
};
</script>

<style lang="less" scoped>
.my-button {
  height: 100px;
}
</style>