<template>
  <div>
    <div class="container">
      <h1>{{ title }}</h1>
      <div class="row">
        <div class="col" v-for="(project, index) in projects" :key="project.id">
          {{ project.title }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import axios from 'axios';
import { resolveTransitionHooks } from 'vue';

export default {
  'name': 'App',
  data() {
    return {
      title: 'Ciao',
      projects: [],
      apiUrl: 'http://127.0.0.1:8000/api'
    }
  },
  methods: {
    getData() {
      axios.get(`${this.apiUrl}/projects`).then((res) => {
        this.projects = res.data.results.data;
      })
    }
  },
  mounted() {
    this.getData();
  }
}
</script>

<style lang="scss" scoped></style>