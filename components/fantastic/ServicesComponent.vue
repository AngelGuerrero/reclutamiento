<template lang="pug">
  .services__wrapper
    .services__content(class="container dev d-flex flex-column justify-content-center")
      .services__header.dev
        h1.services__title(class="dev mb-4") Servicios
      .services__main
        b-row(class="myrow")
          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center")
            img(class="section__image dev" src="~/assets/images/filtro_personal.svg", alt="Filtro de personal")
          b-col(class="col-12 col-md-6")
            .box.dev(class="h-100 d-flex flex-column justify-content-center p-3")
              h3.mb-4 Óptimo proceso de selección de personal
              p.text-white.dev Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

        b-row(class="myrow row-swap")
          b-col(class="col-12 col-md-6")
            .box.dev(class="h-100 d-flex flex-column justify-content-center p-3")
              h3.mb-4 Evaluaciones y pruebas psicométricas
              p.text-white.dev Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center")
            img(class="section__image dev" src="~/assets/images/evaluaciones.svg", alt="Pruebas psicométricas")

        b-row(class="myrow")
          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center")
            img(class="section__image dev" src="~/assets/images/armado_expedientes.svg", alt="Armado del expediente")
          b-col(class="col-12 col-md-6")
            .box.dev(class="h-100 d-flex flex-column justify-content-center p-3")
              h3.mb-4 Armado de expedientes
              p.text-white.dev Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.


        b-row(class="myrow row-swap")
          b-col(class="col-12 col-md-6")
            .box.dev(class="h-100 d-flex flex-column justify-content-center p-3")
              h3.mb-4 Rebacación de documentos
              p.text-white.dev Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center")
            img(class="section__image dev" src="~/assets/images/recabacion_documentos.svg", alt="Recabación de documentos")
    .last

</template>

<script></script>

<style lang="scss" scoped>
.services__wrapper {
  background-color: #0110b3;
  color: white;
  margin-bottom: 100px;
}

.services__content {
  min-height: 70vh;
}

.services__main {
  padding: 50px 0;
}

.last {
  height: 100px;
  background-color: white;
  background-image: url('~assets/images/wavesNegative.svg');
  background-repeat: no-repeat;
  background-size: auto;
  background-position: bottom;
}

.box {
  color: white;
}

.myrow {
  margin-top: 60px;
  min-height: 60vh;
}

.section__image {
  height: 100%;
  max-height: 400px;
}

.row-swap {
  display: flex;
  flex-direction: column-reverse;
  @include media-screen-md {
    flex-direction: row;
  }
}
</style>
