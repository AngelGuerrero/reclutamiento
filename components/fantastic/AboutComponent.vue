<template lang="pug">
  .about__wrapper(class="d-flex justify-content-center align-items-center")
    b-container(class="dev h-100")
      b-row.dev
        b-col(class="dev d-flex flex-column justify-content-center col-12 col-lg-6")
          h1(class="about__title title--square") Nosotros
          img(class="about__image align-self-center mb-3" src="~assets/images/aboutus.svg", alt="AboutUs")
        b-col(class="dev d-flex align-items-center col-12 col-lg-6")
          .box__description(class="shadow-lg")
            h3.mb-3 ¿Quénes somos?
            p.box__text Somos un grupo de emprendedores que iniciamos en el área de reclutamiento de campo, 
              | y decidimos llevar las cosas a un próximo nivel para aumentar nuestro rendimiento,
              | la confiabilidad, la eficiencia y la efectividad en nuestros servicios, automatizando
              | nuestros procesos internos e integrando al mejor personal para la atracción de talento.
</template>

<style lang="scss" scoped>
.about__wrapper {
  // settings
  min-height: 100vh;
  padding: 30px 0;
  background-color: #f1f2f3;
  // presentation
  background-image: url('~assets/images/wave.svg');
  background-repeat: no-repeat;
  background-size: contain;
  background-position: bottom center;
}

.about__title {
  margin-bottom: 50px;
  color: #0110b3;
}

.about__image {
  width: 70%;
  max-width: 400px;
}

.title--square {
  @include media-screen-lg {
    text-align: left;
  }
}

.box__description {
  padding: 30px;
  // border: 1px solid skyblue;
  border-radius: 6px;
  background-color: white;
}

.box__text {
  font-size: 18px;
}
</style>
