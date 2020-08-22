<template lang="pug">
  .contact__wrapper.dev
    .contact__content.container.dev
      b-container
        h1.title Contacto
        b-row.dev
          b-col(class="col-12 col-md-6 dev py-5 d-flex align-items-center align-items-center")
            b-form(class="w-100")
              //- Nombre
              b-form-group(label="Nombre" label-for="input-name")
                b-form-input(type="text"
                            name="input-name"
                            placeholder="Ingresa tu nombre")
              //- Email
              b-form-group(label="Email" label-form="input-email")
                b-form-input(type="email"
                            name="input-email"
                            placeholder="Ingresa tu email"
                )
              //- Message
              b-form-group(label="Mensaje" label-for="input-message")
                b-form-textarea(type="textarea"
                                placeholder="Escribe aquí tu mensaje"
                )
              //- Send button
              b-button(variant="primary" class="btn-block") Enviar mensaje

          b-col(class="col-12 col-md-6 d-flex justify-content-center align-items-center dev")
            img(class="w-100" src="~assets/images/contacto.svg", alt="Contacto")
</template>

<style lang="scss" scoped>
.contact__wrapper {
  min-height: 100vh;
}
</style>
