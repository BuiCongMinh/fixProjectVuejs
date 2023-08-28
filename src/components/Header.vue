<template>
  <div class="header">
    <input type="text" v-model="name" /> <br>
    <input type="checkbox" v-model="status"> ban co dong y 
    <h1>{{ name }}</h1>
  </div>
</template>

<script>

console.log('>>> status',status);

export default {
  data() {
    const toggle = 'Hien'
    const name = 'Viec Can Lam' 
    const status = true
    return { name, status, toggle };
  },

  name: "Header",
};
</script>

<style scoped>
.header {
  background: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
}
</style>