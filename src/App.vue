<template>
  <h1>{{ title }}</h1><br>
  <p>Welcome...</p>

  <div v-if="showModal">
    <Modal @close="toggleModalTwo">

      <template v-slot:links>
        <a href="#">First link</a>
        <a href="#">Second link</a>
      </template>
      <h1>This is under the Slot template</h1>
    </Modal>

  </div><br>
  <button @click="toggleModalTwo">Show Modal</button>
</template>


<script>
import Modal from './components/Modal.vue'

  export default {
    name: 'App',
    components: { Modal },
    data() {
      return {
        title: 'My First Vue Code :)'
      }
    }
  }
</script>

<style>

</style>