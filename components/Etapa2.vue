<template>

    <div>

    
        <p class = "texto">  
            Ao ver que a manada passou, você desce da árvore e começa a explorar a região
            em busca de respostas. Não muito distante dali, você encontra um acampamento
            abandonado e um bilhete com instruções, deixado para trás. Antes que você possa
            alcançar o bilhete, um homem aparece com uma marreta gritando e avançando em
            sua direção. No seu corpo a adrenalina dispara. O que você faz? &#129300;
        </p>
        
        <p class = "opcoes"> Escolha uma das opções:  </p>
        <ul>

            <input class = "rbox1" type="radio" id = "1" name = "Op"  v-model = "opcao" value = "Foge para bem longe">
            <label class = "tbox" for="1" >A. Foge para bem longe</label><br>
            <input class = "rbox2" type="radio" id = "2" name = "Op" v-model = "opcao" value="Pega o bilhete e foge para bem longe">
            <label class = "tbox" for="2">B. Pega o bilhete e foge para bem longe </label><br>
            <input class = "rbox3" type="radio" id = "3" name = "Op" v-model = "opcao" value = "Puxa toda coragem do coração e enfrenta o homem">
            <label class = "tbox" for="3">C. Puxa toda coragem do coração e enfrenta o homem </label><br>
            
        </ul>

        <p class= "resp"> Sua Resposta: </p>
        <input class = "text-input" type = "text" :value = "opcao"><br>

        <button class= "btn" @click="alteraPag(opcao)" > Confirmar </button>
        

      

    </div>
    
</template>

<script>
export default {

    data(){
        return {
            opcao : ""
                }
    },

    methods: {
      alteraPag: function(op){
        
        if (op == "Foge para bem longe"){
        
          window.location.href  = "2/outcome/1"
          
        } else if (op == "Pega o bilhete e foge para bem longe") {

          window.location.href  = "2/outcome/2"
        }

        else if (op == "Puxa toda coragem do coração e enfrenta o homem"){
          
          window.location.href  = "2/outcome/3"
        } else {

          window.alert("Por Favor, escolha uma das opções! ");

        }

      }

    }
    
}
</script>

<style scoped>

.text-input{
  width:350px;
  height: 30px;
}

.texto{

  padding-left: 20%;
  padding-right: 20%;
}

.opcoes{
 padding-top: 15px;
 padding-bottom: 15px;
 font-weight: bold;
}

.resp {
  padding-top: 15px;
}

.tbox{

  margin-left: 5px;
  vertical-align:center;
  text-align: left;

}

.rbox1{

  margin-left: -13.7%;

}

.rbox2{

  margin-left: -7.4%;

}

.rbox3{

  margin-left: -1.9%;

}

.btn {

  margin-top: 15px;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;

}

.btn:hover {
  color: #fff;
  background-color: #3b8070;
}

</style>