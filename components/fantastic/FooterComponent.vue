<template lang="pug">
  .footer__wrapper
    .footer__separator
    .footer__content(class="container")
      b-row
        b-col(class="col-6 col-md-3 mt-5")
          h5.footer__title Menú del sitio
          ul
            li Inicio
            li Nosotros
            li Servicios
            li Vacantes
            li Contacto
            li Acceso
            li Administración
        b-col(class="col-6 col-md-3 mt-5")
          h5.footer__title Redes sociales
          .social__icon
            img(src="~assets/images/logo/icon-facebook.png", alt="alt")
        b-col(class="col-6 col-md-3 mt-5")
          h5.footer__title Empresa
          ul
            li Info.
            li Únete al equipo
            li Nuestra marca
            li Blog
        b-col(class="col-6 col-md-3 mt-5")
          h5.footer__title Recursos
          ul
            li Preguntas frecuentes
            li Condiciones
            li Privacidad
    .made_by(class="py-3")
      b-container(class="h-100 ")
        b-row(class="d-flex align-items-center")
          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center")
            p 2020 © Portal de reclutamiento y selección de personal.
          b-col(class="col-12 col-md-6 justify-content-center align-items-center")
            p.text-center Made by Pink Coders
</template>

<style lang="scss" scoped>
.footer__wrapper {
  background-color: #202020;
  color: white;
}
.footer__content {
  min-height: 60vh;
  padding: 30px;
  color: #7e7e7e;
  ul {
    padding: 0;
    margin: 0;
    li {
      list-style: none;
    }
  }
}

.footer__separator {
  width: 100%;
  height: 100px;
  margin-top: 50px;

  background-color: white;
  background-image: url('~assets/images/waves_separator.svg');
  background-repeat: no-repeat;
  background-size: contain;
  background-position: top center;
}

.footer__title {
  font-size: 17px;
  margin-bottom: 10px;
  color: rgb(173, 173, 173);
  text-transform: uppercase;
}

.social__icon {
  width: 25px;
  img {
    max-width: 100%;
  }
}

.footer__grid {
}

.made_by {
  min-height: 70px;
  background-color: #232f3c;
  p {
    color: #7d8896;
  }
}
</style>
