<template>
  <div>
   <h1>Index users</h1>
   <card-info>
     <p>usuarios disponibles</p>
   </card-info>
   <p>{{ $route.params.id }}</p>
  </div>
</template>

<script>
import cardInfo from '../../components/cardInfo.vue'
export default {
  components: { cardInfo },
  validate(ruta){
    console.log(ruta)
    return /^\d+$/.test(ruta.params.id)
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
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
