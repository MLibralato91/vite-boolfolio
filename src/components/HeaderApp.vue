<template>
  <header>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Boolfolio</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item" v-for="(link, index) in menu">
              <!-- <a class="nav-link active" aria-current="page" href="#">{{ link }}</a> -->
              <router-link :to="{ name: link.routeName }" class="nav-link">
                {{ link.label }}</router-link>
            </li>

          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'HeaderApp',
  data() {
    return {
      menu: [
        {
          label: 'Home',
          routeName: 'home'
        },
        {
          label: 'Projects',
          routeName: 'projects'
        },
        {
          label: 'AboutUs',
          routeName: 'about'
        },
        {
          label: 'Projects',
          routeName: 'contact'
        },

      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>