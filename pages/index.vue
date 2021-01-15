<template>
  <div class="container">
    

     <ul>
      <li v-for="item in recetas" :key="item">
        <NuxtLink :to="'/quiz/' + item">
          {{ item }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      recetas: ["hola", "adios"],
    };
  },
};
</script>
