<template lang="pug">
  .hero__wrapper
    //- Navbar
    NavbarComponent
    //- Hero content
    .hero__content.dev
      .picture.dev
        img(class="ilustration" src="~assets/images/human.svg", alt="ilustration")
      .content__title.dev
        h2.title.dev.title--cursive !Regístrate! Estamos
        h3.title.dev.title--square Contratando
        p.dev.information Tenemos distintas vacantes las cuales puedes aplicar directamente en
          | nuestro sitio ú obtener más información de ellas contactando por este medio o nuestras redes sociales. 
        button(class="snip1582") Ver vacantes
    .social__wrapper
      .container(class="d-flex")
        .icons(class="w-25 d-flex")
          .social__icon
            img(src="~assets/images/logo/icon-facebook.png", alt="alt")
        .simple-icon(class="w-25 mx-auto")
          b-icon(icon="mouse" class="h1")
</template>

<style lang="scss" scoped>
.hero__wrapper {
  // settings
  min-height: 100vh;
  position: relative;
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

.hero__content {
  grid-row: 2;
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;

  @include media-screen-md {
    flex-direction: row;
  }

  .picture {
    width: 25%;
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
    // max-width: 500px;
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
  // max-width: 300px;
  text-align: justify;
  @include media-screen-lg {
    max-width: 500px;
  }
}

.information {
  font-size: 18px;
  @include media-screen-md {
    max-width: 350px;
    font-size: 18px;
  }
}

.social__wrapper {
  grid-row: 3;
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
