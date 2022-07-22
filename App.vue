<script setup>
import {ref, onmounted, computed, watch } from 'vue'

const todos = ref([])
const name = ref('')

const content = ref('')
const category = ref(null)

const todo_asc = computed(() => todos.value.sort((a,b) => {
    return b.createdAt - a.createdAt
} )) 



</script>

<template>
  <main class = "app">

        <section class = 'greeting'>

          <h2 class = "title">

            What's up <input type="text" placeholder=" Your name here" v-model="name" />

          </h2>

        </section>

  </main>

</template>


