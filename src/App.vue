<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <h1>Hello, I'm a Vue Project</h1>
    <button @click="showModal" class="btn">Click me!</button>
    <Modal v-show="isModalVisible" @close="closeModl" />
  </div>
</template>

<script>
import Modal from "./components/A_Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModl() {
      this.isModalVisible = false;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
  color: white;
  background: #000;
  border: 1px solid #828282;
  border-radius: 2px;
  margin: 4px;
  padding: 8px;
  border-radius: 5px;
}
</style>
