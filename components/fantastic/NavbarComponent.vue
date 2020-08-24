<template lang="pug">
  .nav__wrapper
    .nav__hamburguer.dev
      b-icon(icon="justify-left" class="h2 mb-0")
    //- .logo.dev
      img(class="logo__img" src="~assets/images/logo/logo.png", alt="alt")
    ul(class="snip1555 nav__items dev")
      li
        a(href="#" class="nav__item") Nosotros
      li
        a(href="#" class="nav__item") Servicios
      li
        a(href="#" class="nav__item") Vacantes
      li
        a(href="#" class="nav__item") Contacto
      li
        a(href="#" class="nav__item") Acceso

</template>

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
  // background-color: rgba(244, 244, 255, 0.87);
  &:hover {
    background-color: white;
  }
  // breackpoints
  @include media-screen-lg {
    display: flex;
    justify-content: space-around;
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
</style>
