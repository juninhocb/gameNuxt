<template>
    <h1>
     <body v-if="nivel == 1">
        <br><br>
        <NuxtLink 
          to="/play/1"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa1</NuxtLink>
      
        <NuxtLink 
          to="/play/1"
          rel="noopener noreferrer"
          class="btnBr"
        > Etapa2</NuxtLink>

        <NuxtLink 
          to="/play/1"
          rel="noopener noreferrer"
          class="btnBr"
        > Etapa3</NuxtLink>
    </body>

    <body v-if="nivel == 2">
        <br><br>
        <NuxtLink 
          to="/play/1"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa1</NuxtLink>
      
        <NuxtLink 
          to="/play/2"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa2</NuxtLink>

        <NuxtLink 
          to="/play/2"
          rel="noopener noreferrer"
          class="btnBr"
        > Etapa3</NuxtLink>
    </body>

    <body v-if="nivel == 3">
        <br><br>
        <NuxtLink 
          to="/play/1"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa1</NuxtLink>
      
        <NuxtLink 
          to="/play/2"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa2</NuxtLink>

        <NuxtLink 
          to="/play/3"
          rel="noopener noreferrer"
          class="btnBr1"
        > Etapa3</NuxtLink>
    </body>

    </h1>

   

</template>

<script>
export default {
    props: {

        nivel: Number

    }
}
</script>

<style scoped>

.btnBr {

  margin-top: 65px;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;


}

.btnBr:hover {
  color: #fff;
  background-color: #3b8070;
}

.btnBr1 {

  margin-top: 65px;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #f6f8f8;
  text-decoration: none;
  padding: 10px 30px;
  background-color: #3b8070;


}

</style>