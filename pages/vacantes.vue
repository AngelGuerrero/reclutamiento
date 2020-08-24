<template lang="pug">
  //- Landing page 'Fantastic design'
  .vacantes__wrapper.dev
    NavbarComponent
    .vacantes__content
      JobsComponent
</template>

<script>
export default {
  layout: 'fantastic/FantasticLayout',
}
</script>

<style lang="scss" scoped>
.vacantes__content {
  padding-top: 50px;
  min-height: 100vh;
  background-color: rgba(33, 25, 143, 0.089);
}
</style>
