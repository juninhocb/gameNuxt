<template >

    <div class= "container">

         <div>
            <Logo />
            <h1 class="title" v-if="id2.id2 ==  1">
             Game Over! &#128549;
             </h1>

            <h2 class="title" v-if = "id2.id2 == 2" >
             Game Over! &#128549;
             </h2>

            <h3 class="title" v-if = "id2.id2 == 3" >
            Sucesso, Você está quase lá! &#128079;
            </h3>

             
            <div class= "componentes">
   
    <body v-if="id2.id2 == 1">


        <font class= "text">
        Você consegue fugir do local e voltar à cidade, porém sem nenhuma ideia
        de quem o atacou. Você continua tentando juntar as peças do
        quebra-cabeças. 2 semanas depois você morre atropelado, “acidentalmente”,
        ao sair de casa.<br><br>
        </font>


        
        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class="btover"
        > Voltar ao Inicio </NuxtLink>
        
    </body>

    <body v-if="id2.id2 == 2" >

        <font class= "text">
        O homem lhe alcançou enquanto você tentava pegar o bilhete e lhe acertou
        uma marretada. Você morreu. <br><br>
        </font>

        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class="button--green"
        > Voltar ao Inicio </NuxtLink>

    </body>

    <body v-if="id2.id2 == 3" >

        <font class= "text">
        Você consegue desviar da primeira marretada do homem, que fica ocioso
        por um curto período, o suficiente para você acertá-lo em cheio na cabeça e
        apagá-lo no chão. <br><br> 
        </font>

        <NuxtLink 
          to="/play/3"
          rel="noopener noreferrer"
          class = "btover"

        > Continuar </NuxtLink>
        
    </body>

    

   
    
                </div> 
          </div>
    </div>

  

</template>



<script>

export default {
    data(){
        return {
            id2 : this.$route.params
            
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