<template>
  <div class="parent">
    <h1>Hi Guys, Welcome</h1>
    <ChildComponent @dataClicked="handleDataClick" />
    <div v-if="displayedData" class="displayed-data">
      <h2>Fun fact about programming:</h2>
      <p>{{ displayedData }}</p>
    </div>
    <slot name="additionalContent"></slot>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent
  },
  data() {
    return {
      displayedData: ''
    };
  },
  methods: {
    handleDataClick(data) {
      this.displayedData = data;
    }
  }
}
</script>

<style scoped>
.parent {
  background: linear-gradient(135deg, #f0f0f0 0%, #d4fc79 100%);
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  text-align: center;
}

h1, h2 {
  color: #2c3e50;
}

.displayed-data {
  margin-top: 20px;
  padding: 10px;
  background-color: rgb(0, 0, 0);
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
</style>
