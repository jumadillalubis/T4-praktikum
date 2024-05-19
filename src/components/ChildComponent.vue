<template>
  <div class="child">
    <button @click="emitData">Send Data</button>
    <div v-if="showMessage" class="message-box">Hello from Zulfiana Jumadilla Lubis!</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMessage: false
    };
  },
  methods: {
    emitData() {
      this.$emit('dataClicked', 'The worlds first programmer was a woman');
      this.showMessage = !this.showMessage;
    }
  }
}
</script>

<style scoped>
.child {
  text-align: center;
}

button {
  padding: 12px 25px;
  background-color: #1abc9c;
  color: white;
  border: none;
  border-radius: 25px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s;
}

button:hover {
  background-color: #16a085;
  transform: scale(1.1);
}

.message-box {
  margin-top: 20px;
  padding: 10px;
  background-color: #1abc9c;
  color: rgb(0, 0, 0);
  border-radius: 10px;
}
</style>
