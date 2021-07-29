<template>
  <div>
    <h1>Usuarios Principal!!</h1>
    <div>
      <ul>
        <li v-for="user in users" :key="user.id">
          <!-- <nuxt-link :to="'users/'+user.name">{{user.name}}</nuxt-link> -->
          <nuxt-link :to="{ name: 'users-id', params: { id: user.id } }">{{
            user.name
          }}</nuxt-link>
        </li>
      </ul>
    </div>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { name: "Lucia", id: 1 },
        { name: "Jaime", id: 2 },
        { name: "Eliza", id: 3 },
        { name: "Andres", id: 4 },
      ],
    };
  },
};
</script>