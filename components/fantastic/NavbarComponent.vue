<template lang="pug">
  .nav__wrapper
    .nav__hamburguer(@click="showAsideMenu = !showAsideMenu")
      b-icon(icon="justify-left" class="h1 mb-0")
    ul(class="snip1555 nav__items dev")
      li(v-for="link in menu" :key="link.id")
        nuxt-link(:to="link.route" class="nav__item") {{ link.title }}
    //- Aside navbar
    .backgrop(v-show="showAsideMenu" @click="showAsideMenu = !showAsideMenu")
    .aside_navbar(v-if="showAsideMenu")
      .aside__header(class="d-flex align-items-center mb-3")
        h2.header__title(class="flex-grow-1 pl-3 mb-0 mx-auto") Menú
        .btn--close(@click="showAsideMenu = !showAsideMenu"
                    class="p-3 d-flex justify-content-center align-items-center bg-dark color-white")
          b-icon(icon="x" class="h2 mb-0")
      b-container
        ul(class="snip1555 d-flex flex-column m-0 p-0 w-100")
          li(v-for="link in menu" :key="link.id" class="nav__item--mobile")
            nuxt-link(:to="link.route") {{ link.title }}
</template>

<script>
export default {
  data() {
    return {
      showAsideMenu: true,
      menu: [
        { title: 'Inicio', route: '/' },
        { title: 'Nosotros', route: '/#nosotros' },
        { title: 'Servicios', route: '/#servicios' },
        { title: 'Vacantes', route: '/vacantes' },
        { title: 'Contacto', route: '/#contacto' },
        { title: 'Acceso', route: '/login' },
      ],
    }
  },
}
</script>

<style lang="scss">
.nav__wrapper {
  grid-row: 1;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  min-height: 80px;
  // presentation
  font-family: 'Baloo Tamma 2', cursive;
  font-size: 18px;
  &:hover {
    background-color: white;
  }
  // breakpoints
  @include media-screen-lg {
    // display: flex;
    // justify-content: space-around;
  }

  .nav__hamburguer {
    display: block;
    margin: 0 10px;
    color: #6c63ff;
    &:hover {
      cursor: pointer;
      color: #ea16f1;
    }
    @include media-screen-lg {
      display: none;
    }
  }

  .nav__items {
    display: none;
    margin: 0;
    @include media-screen-lg {
      display: flex;
      justify-content: space-between;
      align-content: center;
    }
  }
  .nav__item {
    color: #6c63ff;
    display: flex;
    align-items: center;
    transition: all 0.5s;
    cursor: pointer;

    &:active {
      color: purple;
    }
    &:hover {
      color: #fc0d7c;
      text-decoration: none;
    }
  }
}

.logo {
  display: none;
  @include media-screen-lg {
    display: block;
    max-width: 90px;
    text-align: center;
    img {
      width: 30%;
      height: 30%;
    }
  }
}

.separator {
  margin: 0 15px;
  border-radius: 15px;
  border: 1px solid #757575;
  @include media-screen-md {
    display: none;
  }
}

.aside_navbar {
  width: 250px;
  height: 100%;
  position: fixed;
  z-index: 10;
  top: 0;
  left: 0;
  background-color: #0110b3;
  color: white;
}

.backgrop {
  width: 100%;
  height: 100%;
  position: fixed;
  z-index: 9;
  top: 0;
  left: 0;
  backdrop-filter: blur(2px);
}

.nav__item--mobile {
  width: 40%;
  a {
    transition: color 0.5s;
    &:hover {
      color: #fce40d;
    }
  }
}

.header__title {
  color: #fce40d;
}

.btn--close {
  cursor: pointer;
}
</style>
