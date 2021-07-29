<template>
  <div>
    <div>
        <h1>Layout</h1>
      <ul>
        <li v-for="ruta in rutas" :key="ruta.label">
          <nuxt-link :to="ruta.ruta">{{ruta.label}}</nuxt-link>
        </li>
      </ul>
    </div>
    <Nuxt />
    <footer>
      <div>
        &copy; 2021
      </div>
    </footer>
  </div>
</template>


<script>
export default {
  data(){
    return{
      rutas:[
        {ruta:"/", label:"Inicio"},
        {ruta:"/users/1", label:"Usuarios"},
        {ruta:"/carros", label:"Carros"},
        {ruta:"/motos", label:"Motos"},
        {ruta:"/contact", label:"Contacto"},
      ]
    }
  }
}
</script>

<style scoped>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
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

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

ul{
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
}

li{   
  float: none;
}

li a{
  display: block;
  padding: 8px;
  background-color: rgb(36, 3, 5);
  color: #fff;
}

footer{
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  background-color: rgb(36, 3, 5);
  color: #fff;
  text-align: center;
}

</style>
