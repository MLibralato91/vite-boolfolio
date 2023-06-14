<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <div class="row">
      <div class="col-3" v-for="(project, index) in projects " :key="project.id">
        <div class="card">
          <img class="card-img-top" :src="project.image" :alt="project.title">
          <div class="card-body">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <p class="card-text">{{ project.type.name }}</p>
            <a href="#" class="btn btn-primary">Dettagli</a>
          </div>
        </div>
      </div>
    </div>
    <nav aria-label="Page navigation example">
      <ul class="pagination">
        <li class="page-item"><button class="page-link" @click="getData(currentPage - 1)">Previous</button></li>
        <li class="page-item" v-for="   n    in    lastPage   "><button class="page-link" @click="getData(n)">{{ n
        }}</button>
        </li>

        <li class="page-item"><button class="page-link" @click="getData(currentPage + 1)">Next</button></li>
      </ul>
    </nav>
  </div>
</template>

<script>
import axios from 'axios';


export default {
  'name': 'ProjecsList',
  data() {
    return {
      title: 'My Projects',
      projects: [],
      apiUrl: 'http://127.0.0.1:8000/api',
      currentPage: 1,
      lastPage: null,
    }
  },
  methods: {
    getData(numPage) {
      axios.get(`${this.apiUrl}/projects`, {
        params: {
          'page': numPage
        }
      }).then((res) => {
        //console.log(res);
        this.projects = res.data.results.data;
        this.currentPage = res.data.results.current_page;
        this.lastPage = res.data.results.last_page;
      })
    }
  },
  mounted() {
    this.getData();
  }
}
</script>

<style lang="scss" scoped></style>