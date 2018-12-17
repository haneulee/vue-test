<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button type="button" class="btn" @click="showModal">Open Modal!</button>
    <modal v-show="isModalVisible" @close="closeModal"/>
  </div>
</template>

<script>
import modal from "@/components/modal";

export default {
  name: "HelloWorld",
  components: {
    modal
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      isModalVisible: false
    };
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
</style>
