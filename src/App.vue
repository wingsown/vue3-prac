<template>
  <h1>{{ title }}</h1>
  <div to=".modals" v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up</a>
        <a href="#">More info</a>
      </template>
      <h1>Hello</h1>
      <p>This is the content</p>
    </Modal>
  </div>

  <button @click="toggleModal">Open Modal</button>
  
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: 'My First Vue App',
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    }
  }
  
}
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
</style>
