<template >

    <div class= "container">

         <div>
            <Logo />
            <h1 class="title" v-if="id.id ==  1">
             Game Over! &#128549;
             </h1>

            <h2 class="title" v-if = "id.id == 2" >
             Sucesso! &#128079;
             </h2>

            <h2 class="title" v-if = "id.id == 3" >
            Game Over! &#128549;
            </h2>

             
            <div class= "componentes">
   
    <body v-if="id.id == 1">


        <font class= "text">
        A sua corrida não foi suficiente para superar a da manada. Você morreu
        atropelado. <br><br>
        </font>


        
        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class="btover"
        > Voltar ao Inicio </NuxtLink>
        
    </body>

    <body v-if="id.id == 2" >

        <font class= "text">
        Você sobe na árvore e escapa por pouco da manada. <br><br>
        </font>

        <NuxtLink 
          to="/play/2"
          rel="noopener noreferrer"
          class="button--green"
        > Continuar </NuxtLink>

    </body>

    <body v-if="id.id == 3" >

        <font class= "text">
        Os búfalos podem até ter acreditado, mas isso não os impediu de passar
        por cima de você. Morreu atropelado. <br><br> 
        </font>

        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class = "btover"

        > Voltar ao Inicio </NuxtLink>
        
    </body>

    

   
    
                    </div> 
            </div>
    </div>

  

</template>



<script>

export default {
    data(){
        return {
            id : this.$route.params
            
                }
    
    }



    }
</script>

<style scoped>

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

.componentes {
  padding-top: 30px;
}

.text {

    font-size: 30px;
}

.btover {
  
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
  

}

.btover:hover {
  color: #fff;
  background-color: #3b8070;
}

</style>