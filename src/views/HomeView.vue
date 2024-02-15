<script setup>
import phoneData from '../data.json'
import {ref} from 'vue'

const phones=ref(phoneData)
</script>

<template>
  <main class="container">
 
    <h1>Our Phones</h1>
    <div class="cards">
      <div v-for="phone in phones" :key="phone.id"   class="card">
        <h1>{{ phone.make }}</h1>
        <p>₹{{ phone.price }}</p>
      </div>
    </div>
  </main>
</template>


<style scoped>
  .cards {
  display: flex;
  width: 1000px;
  flex-wrap: wrap;
  margin-top: 50px;
  justify-content: center;
}

.card {
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.207);
  padding: 15px;
  width: 150px;
  margin-right: 15px;
  cursor: pointer;
  margin-bottom: 20px;

}


</style>