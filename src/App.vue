<template>
  <div id="app">
    <h1>Pemrograman Berbasis Komponen</h1>
    <ParentComponent>
      <!-- Slot for displaying additional content -->
      <template v-slot:additionalContent>
        <div class="additional-content">
          
        </div>
      </template>
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent
  }
}
</script>

<style>
#app {
  font-family: 'Arial', sans-serif;
  text-align: center;
  margin-top: 50px;
}

h1 {
  color: #34495e;
  font-size: 3em;
}

.additional-content {
  margin-top: 20px;
  text-align: center;
}

.decorative-box {
  margin-top: 20px;
  padding: 20px;
  background-color: #e74c3c;
  color: white;
  border-radius: 15px;
  display: inline-block;
}
</style>
