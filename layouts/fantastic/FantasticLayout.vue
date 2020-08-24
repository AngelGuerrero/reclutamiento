<template>
  <!-- Fantastic layout -->
  <div>
    <Nuxt />
  </div>
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

<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

p {
  font-size: 18px;
  color: #3b3b3b;
}

.title {
  color: #0110b3;
  margin-bottom: 30px;
}

.title--cursive {
  font-family: 'Lobster', cursive;
  font-weight: lighter;
  font-size: 30px;
  color: #ea16f1;
  @include media-screen-lg {
    font-size: 35px;
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

.dev {
  // border: 1px solid tomato;
}

//
// Button snippet snip1582
//
$snip1582__color: #3735c4;
.snip1582 {
  background-color: $snip1582__color;
  border: none;
  color: #ffffff;
  cursor: pointer;
  display: inline-block;
  font-family: 'BenchNine', Arial, sans-serif;
  font-size: 0.5em;
  font-size: 16px;
  line-height: 1em;
  margin: 15px 40px;
  outline: none;
  padding: 12px 40px 10px;
  position: relative;
  text-transform: uppercase;
  font-weight: 700;
  @include media-screen-md {
    font-size: 1em;
    font-size: 18px;
  }
}

.snip1582:before,
.snip1582:after {
  border-color: transparent;
  -webkit-transition: all 0.25s;
  transition: all 0.25s;
  border-style: solid;
  border-width: 0;
  content: '';
  height: 24px;
  position: absolute;
  width: 24px;
}

.snip1582:before {
  border-color: $snip1582__color;
  border-top-width: 2px;
  left: 0px;
  top: -5px;
}

.snip1582:after {
  border-bottom-width: 2px;
  border-color: $snip1582__color;
  bottom: -5px;
  right: 0px;
}

.snip1582:hover,
.snip1582.hover {
  background-color: $snip1582__color;
}

.snip1582:hover:before,
.snip1582.hover:before,
.snip1582:hover:after,
.snip1582.hover:after {
  height: 100%;
  width: 100%;
}

// Snippet snip1555
.snip1555 {
  // font-family: 'Muli', Arial, sans-serif;
  // font-size: 16px;
  // letter-spacing: 1.5px;
  // line-height: 1em;
  // margin: 15px 30px;
  // text-transform: uppercase;
}
.snip1555 li {
  display: inline-block;
  list-style: outside none none;
  margin: 0.5em 0.6em;
  padding: 12px 15px;
  position: relative;
}
.snip1555 li a {
  color: #fff;
  text-decoration: none;
}
.snip1555 li:before,
.snip1555 li:after {
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
  height: 2px;
  width: 35%;
  background-color: #528cb3;
  position: absolute;
  content: '';
  opacity: 0;
}
.snip1555 li:before {
  top: 0;
  left: 0;
}
.snip1555 li:after {
  bottom: 0;
  right: 0;
}
.snip1555 li:hover:before,
.snip1555 li.hover:before,
.snip1555 li:hover:after,
.snip1555 li.hover:after {
  opacity: 1;
}
.snip1555 li:hover:before,
.snip1555 li.hover:before {
  left: 65%;
}
.snip1555 li:hover:after,
.snip1555 li.hover:after {
  right: 65%;
}
</style>
