<template>
  <div>
   <h1>Index</h1>
   <div>
     <nuxt-link to="/users">Users</nuxt-link>
     <nuxt-link to="/users/one">One</nuxt-link>
     <nuxt-link :to="{name:'users-one'}">One</nuxt-link>
     <nuxt-link :to="{name:'contact'}">Contact</nuxt-link>
   </div>
   <div><button @click="goto({name:'users-one'})">One</button></div>
   <hr>
   <div>
     <ul>
       <li v-for="user in users" :key="user.id">
         <!-- <nuxt-link :to="'users/'+user.name">{{user.name}}</nuxt-link> -->
         <nuxt-link :to="{name:'users-id', params:{id:user.id}}">{{user.name}}</nuxt-link>
       </li>
     </ul>
   </div>
   <hr>
   <div>
     <ul>
       <li v-for="product in products" :key="product.id + 'cat'">
         <nuxt-link :to="'/'+product.categoria">{{product.categoria}}</nuxt-link>
       </li>
     </ul>
   </div>
   <div>
     <card-info>
       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis error, fugiat accusamus illo cumque eius libero ad unde culpa nesciunt, at enim? Officia excepturi fugit ab aliquid minima at a.</p>
       <p>Consequuntur unde saepe esse nihil perspiciatis natus, sequi, deleniti voluptatem nobis in quisquam. Quaerat dolor veritatis cum expedita quibusdam dolore aliquid beatae recusandae neque? Ut sequi dolores voluptatem at asperiores.</p>
     </card-info>
   </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      users:[
        {name:"Lucia", id:1},
        {name:"Jaime", id:2},
        {name:"Eliza", id:3},
        {name:"Andres", id:4}
      ],
      products:[
        {categoria:"Carros", id:1},
        {categoria:"Motos", id:2},
      ]
    }
  },
  methods:{
    goto(path){
      //this.$router.push('/users')
      //this.$router.push({name:'contact'})
      this.$router.push(path)
    }
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
