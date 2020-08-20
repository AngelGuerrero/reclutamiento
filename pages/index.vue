<template>
  <div class="container">
    <div>
      <div class="logo__wrapper">
        <Logo />
      </div>
      <h1 class="title">
        Plataforma de reclutamiento y selección de personal
      </h1>
      <h3 class="text-danger">Sitio web en construcción</h3>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.logo__wrapper {
  display: flex;
  align-items: center;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
