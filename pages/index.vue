<template>
  <div>
    <p>{{ count }}</p>
    <button @click="increment">Lisää</button>
  </div>
</template>

<script setup lang="ts">
import Vue from 'vue'
export default Vue.extend({
  head: {
    title: 'Testi title',
  },
  data() {
    return {
      testi: 'hello world',
      count: 0,
    }
  },
  methods: {
    increment(): void {
      this.count++
    },
  },
})
</script>
