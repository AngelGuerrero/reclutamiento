<template lang="pug">
  .jobs__wrapper
    .container
      header.jobs__header(class="mb-5")
        h2.header__title Vacantes
      .jobs__content.dev
        b-row.job(class="border rounded align-content-center py-3 mb-4" v-for="(job, index) in jobs" :key="job.id")
          b-col(class="col-12 col-lg-3 d-flex justify-content-center align-items-center")
            img(class="image mb-4 rounded" :src="job.image", :alt="job.altImage")
          b-col(class="col-12 col-lg 9")
            header
              h3.job__title {{ job.title }}
              p(class="text-muted") {{ job.salary }}
            p.job__desc {{ job.mainDescription }}
            .buttons
              b-row
                b-col
                  b-button(size="sm" v-b-toggle="'job-collapse-' + index") Información
                b-col
                  b-button(size="sm") Enviar CV
                b-col
                  b-button(size="sm") Guardar
            b-collapse(:id="'job-collapse-' + index" class="container p-3 mt-5")
              p Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          image: '/images/saludo.jpg',
          altImage: '',
          title: 'Auxiliar de almacén',
          salary: '$6,000 mensuales',
          mainDescription:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.job {
  background-color: white;
}

.header__title {
  color: #0110b3;
}

.image {
  width: 100%;
}
</style>
