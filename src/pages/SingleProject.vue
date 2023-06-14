<template>
  <div v-if="project">
    <div class="col-3 ">
      <div class="cardCarousel">
        <div class="boxImg">
          <img :src="project.image" alt="">
        </div>
        <div class="title d-flex justify-content-between small">
          <h6 class="fw-bolder">{{ project.title }}</h6>
          <p> role </p>
        </div>
      </div>
    </div>
  </div>

  <div v-else>
    <LoaderApp />
  </div>
</template>

<script>
import axios from 'axios';
import LoaderApp from '../components/LoaderApp.vue';
export default {
  name: 'SingleProject',
  components: {
    LoaderApp,
  },
  data() {
    return {
      project: null,
      apiUrl: 'http://127.0.0.1:8000/api'
    }
  },
  methods: {

    getProject() {
      axios.get(`${this.apiUrl}/projects/${this.$route.params.slug}`).then((res) => {
        if (res.data.success) {
          this.project = res.data.results;
        } else {
          this.$router.push({ name: 'not-found' })
        }
      })
    }
  },
  mounted() {
    this.getProject();
  }

}
</script>

<style lang="scss" scoped>
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}

.cardCarousel {
  border-radius: 20px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

}

.title {
  padding: 20px;
  padding-top: 30px;
}
</style>