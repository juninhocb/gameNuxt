<template >

    <div class= "container">

         <div>
            <Logo />
            <h1 class="title" v-if="id3.id3 ==  1">
             Parabéns, você venceu o jogo! &#128640;
             </h1>

            <h2 class="title" v-if = "id3.id3 == 2" >
             Game Over! &#128549;
             </h2>

            <h3 class="title" v-if = "id3.id3 == 3" >
            Game Over! &#128549;;
            </h3>

             
            <div class= "componentes">
   
    <body v-if="id3.id3 == 1">


        <font class= "text">
        Você informa a polícia o que aconteceu e passa a localização do
        laboratório. Chegando lá ela se depara com um sítio de produção de cocaína
        e prende todos os presentes. As evidências sugerem que você ainda pode
        estar em perigo, por este motivo a polícia lhe coloca no programa de
        proteção à testemunha e você sobrevive para vivenciar uma nova história.
        Parabéns, você ganhou!<br><br>
        </font>


        
        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class="btover"
        > Voltar ao Inicio </NuxtLink>
        
    </body>

    <body v-if="id3.id3 == 2" >

        <font class= "text">
        Você amarra o homem e se dirige ao laboratório. Você entra
        silenciosamente e consegue chegar ao salão principal, onde você observa
        aproximadamente umas 10 pessoas. Um passo em falso entrega a sua
        posição e você é alvejado. Você morreu.<br><br>
        </font>

        <NuxtLink 
          to="/"
          rel="noopener noreferrer"
          class="button--green"
        > Voltar ao Inicio </NuxtLink>

    </body>

    <body v-if="id3.id3 == 3" >

        <font class= "text">
        Você mata o homem, pega a marreta e se dirige ao laboratório. Ao avistar
        2 guardas na entrada, confiante de si e seus feitos recentes, você corre na
        direção dos guardas, segurando a marreta com as duas mãos levantadas
        acima da sua cabeça e gritando “LEEROY JEENKINS!!!!”. Infelizmente, o
        efeito surpresa foi prejudicado e os guardas não tiveram dificuldade em
        alvejá-lo. Você morreu. <br><br> 
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
            id3 : this.$route.params
            
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