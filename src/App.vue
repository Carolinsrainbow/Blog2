<template>
  <div id="app">
    <nav class="navbar navbar-dark navbar-expand-lg fixed-top" id="mainNav">
      <div class="container">
        <a class="navbar-brand">V8</a>
        <button
          data-toggle="collapse"
          data-target="#navbarResponsive"
          class="navbar-toggler"
          aria-controls="navbarResponsive"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fa fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="nav navbar-nav ml-auto" id="menu-v8">
            <li class="nav-item" role="presentation">
              <router-link :to="{ name: 'Portada' }">Portada</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link :to="{ name: 'SobreMi' }">Sobre mí</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link to="/Contacto">Contacto</router-link>
            </li>
            <li class="nav-item" role="presentation">
              <router-link to="/Post/1">Último post</router-link>
            </li>
                  <li class="nav-item" role="presentation">
              <router-link to="/administrador/">Administrador</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
   <transition name="mi-transicion">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.mi-transicion-enter-active,
.mi-transicion-leave-active {
  transition: opacity 0.5s;
}
.mi-transicion-enter,
.mi-transicion-leave-to {
  opacity: 0;
  padding: 30px;
}
.mi-transicion-to,
.mi-transicion-leave {
  opacity: 1;
}
</style>
