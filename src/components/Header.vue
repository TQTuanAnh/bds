<template>
  <header>
    <nav class="navbar navbar-expand-sm navbar-dark bg-dark" role="navigation">
      <div class="container-fluid d-flex justify-content-between align-items-center">
        <!-- Brand and toggle get grouped for better mobile display -->
        <router-link to="/" class="navbar-brand mr-auto">THANHPHATREAL</router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTop" aria-controls="navbarTop" aria-expanded="false" aria-label="Toggle navigation" @click="toggleNavbar">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse flex-grow-0" id="navbarTop" :class="{show: isNavOpen}">
          <ul class="nav navbar-nav">
            <router-link
              to="/cardDetails"
              class="nav-item"
              active-class="active"
            >
              <a class="nav-link">Login</a>
            </router-link>
            <li class="li-pointer nav-item">
              <a class="nav-link">Logout</a>
            </li>
            <router-link to="/cardDetails" class="nav-item">
              <a class="nav-link">Register</a>
            </router-link>
            <li>
              <router-link to="/cardDetails" class="btn btn-success navbar-btn">
                Card
                <span class="badge badge-light">{{
                  $store.state.card.length
                }}</span>
              </router-link>
            </li>
          </ul>
        </div>
      </div>
      <!-- /.container -->
    </nav>
  </header>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Header',
  data () {
    return {
      isNavOpen: false
    }
  },
  methods: {
    toggleNavbar () {
      this.isNavOpen = !this.isNavOpen
    }
  }
}
</script>

<style lang="scss" scoped>
header {
  background-color: #dabb42;
  h2 {
    text-shadow: -1px 3px 2px rgba(0, 0, 0, 0.3);
    &.cursor {
      cursor: pointer;
    }
  }
}

.flex-grow-0 {
    flex-grow: 0 !important;
}
</style>
