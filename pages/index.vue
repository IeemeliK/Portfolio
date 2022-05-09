<template>
  <div>
    <div class="grid place-content-center">
      <div class="place-content-center">
        <h3 class="font-bold p-5 text-center">Tässä on tekstiä</h3>
        <ul
          class="leading-tight font-semibold bg-transparent border-4 rounded-md text-center"
        >
          <li v-for="testi of testit" :key="testi.id">
            {{ testi.name }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Vue from 'vue'
import axios from 'axios'

export default Vue.extend({
  head: {
    title: 'Testi title',
  },
  data() {
    return {
      testit: [],
      count: 0,
    }
  },
  methods: {
    increment(): void {
      this.count++
    },
  },
  async mounted() {
    try {
      const res = await axios.get('http://localhost:3001/testeja')
      this.testit = res.data
    } catch (e) {
      console.error(e)
    }
  },
})
</script>
