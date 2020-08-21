<template lang="pug">
  .hero__wrapper
    .nav__wrapper
      .nav__hamburguer.dev
        b-icon(icon="justify-left" class="h2 mb-0")
      .logo.dev
        img(class="logo__img" src="~assets/images/logo/logo.png", alt="alt")
      ul(class="snip1555 nav__items dev")
        li
          a(href="#" class="nav__item") Nosotros
        li
          a(href="#" class="nav__item") Vacantes
        li
          a(href="#" class="nav__item") Bolsa de trabajo
        li
          a(href="#" class="nav__item") Administración
    //- Herro content
    .hero__content.dev
      .picture.dev
        img(class="ilustration" src="~assets/images/human.svg", alt="ilustration")
      .content__title.dev
        h2.title.dev.title--cursive !Regístrate! Estamos
        h3.title.dev.title--square Contratando
        p.dev.information Tenemos distintas vacantes las cuales puedes aplicar directamente en nuestro sitio ú obtener más información de ellas contactando por este medio o nuestras redes sociales. 
        button(class="snip1582") Ver vacantes
    .social__wrapper
      .container(class="d-flex")
        .icons(class="w-25 d-flex")
          .social__icon
            img(src="~assets/images/logo/icon-facebook.png", alt="alt")
        .simple-icon(class="w-25 mx-auto")
          b-icon(icon="mouse" class="h1")
</template>

<script>
export default {
  head: {
    link: [
      {
        rel: 'stylesheet',
        href:
          'https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@500&display=swap',
      },
      {
        rel: 'stylesheet',
        href:
          'https://fonts.googleapis.com/css2?family=Baloo+Tamma+2:wght@500&display=swap',
      },
      {
        rel: 'stylesheet',
        href: 'https://fonts.googleapis.com/css2?family=Lobster&display=swap',
      },
    ],
  },
}
</script>

<style lang="scss" scoped>
@import url('@/assets/scss/helpers.scss');

.hero__wrapper {
  // settings
  height: 100vh;
  // display
  display: grid;
  // grid-template-columns: repeat(6, fr);
  grid-template-columns: repeat(1, fr);
  grid-template-rows: 80px auto 70px;
  // presentation
  background-image: url('~assets/images/background_animate.svg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

.nav__wrapper {
  // display
  display: flex;
  align-items: center;
  // presentation
  font-family: 'Baloo Tamma 2', cursive;
  // breackpoints
  @include media-screen-md {
    padding: 0 100px;
    display: flex;
    justify-content: space-between;
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

.hero__content {
  grid-row: 2;
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;

  @include media-screen-md {
    flex-direction: row;
  }

  .picture {
    margin: auto;
    display: block;

    @include media-screen-md {
      width: 50%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    .ilustration {
      width: 100%;
      @include media-screen-md {
        width: 60%;
        max-width: 250px;
      }
    }
  }

  .content__title {
    // settings
    width: 80%;
    max-width: 500px;
    margin: auto;
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    // presentation

    @include media-screen-md {
      // settings
      width: 50%;
      max-width: none;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
}

.title,
.information {
  max-width: 300px;
  text-align: justify;
  @include media-screen-lg {
    max-width: 500px;
  }
}

.information {
  font-size: 16px;
  @include media-screen-md {
    max-width: 350px;
    font-size: 18px;
  }
}

.title--cursive {
  font-family: 'Lobster', cursive;
  font-weight: lighter;
  font-size: 30px;
  color: #ea16f1;
  @include media-screen-lg {
    font-size: 45px;
    text-align: center;
  }
}
.title--square {
  font-family: 'Montserrat', sans-serif;
  font-weight: bold;
  font-size: 30px;
  text-transform: uppercase;
  color: #1c1ce7;
  @include media-screen-lg {
    font-size: 45px;
    text-align: center;
  }
}
.social__wrapper {
  grid-row: 3;
  background-color: rgba(226, 246, 255, 0.486);
  .social__icon {
    margin: 0 20px;
    display: flex;
    align-items: center;
    cursor: pointer;
    img {
      width: 25%;
    }
  }
}
</style>
