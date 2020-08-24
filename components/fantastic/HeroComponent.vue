<template lang="pug">
  .hero__wrapper
    //- Navbar
    NavbarComponent
    //- Hero content
    .hero__content
      b-container(class="h-100 d-flex align-items-center")
        b-row
          b-col(class="col-12 col-md-6 mb-4")
            img(class="picture" src="~assets/images/human.svg", alt="ilustration")
          b-col(class="col-12 col-md-6 d-flex flex-column align-items-center")
            h2.title(class="dev title--cursive text-center") Hay empresas que están
            h3.title(class="dev title--square text-center") Contratando
            .box-description(class="text-justify p-3 rounded shadow-lg my-2")
              p ¡Regístrate! Tenemos distintas vacantes las cuales puedes aplicar directamente en
                |  nuestro sitio u obtener más información de ellas contactando por este medio o nuestras redes sociales. 
            button(class="snip1582") Ver vacantes

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

.picture {
  max-width: 190px;
  margin: auto;
  display: block;

  @include media-screen-md {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.ilustration {
  width: 100%;
  @include media-screen-md {
    width: 60%;
    max-width: 250px;
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

.box-description {
  background-color: rgba(1, 16, 179, 0.769);
  p {
    color: white;
  }
}
</style>
