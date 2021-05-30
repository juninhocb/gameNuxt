<template>

    <div>

    
        <p class = "texto">  
            Você acordou na floresta tonto e com uma grande dor de cabeça, sem nenhuma
            memória de como foi parar ali. Um barulho cada vez mais intenso foi o que
            despertou você desse apagão. Após abrir os olhos e levantar-se, você observa uma
            manada de búfalos vindo em sua direção, a pouquíssimos metros de distância. O
            que você faz? &#129300;
        </p>
        
        <p class = "opcoes"> Escolha uma das opções:  </p>
        <ul>

            <input class = "rbox1" type="radio" id = "1" name = "Op"  v-model = "opcao" value = "Corre o mais rápido possível">
            <label class = "tbox" for="1" >A. Corre o mais rápido possível</label><br>
            <input class = "rbox2" type="radio" id = "2" name = "Op" v-model = "opcao" value="Sobe na árvore">
            <label class = "tbox" for="2">B. Sobe na árvore </label><br>
            <input class = "rbox3" type="radio" id = "3" name = "Op" v-model = "opcao" value = "Se finge de morto">
            <label class = "tbox" for="3">C. Se finge de morto </label><br>
            
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
        
        if (op == "Sobe na árvore"){
        
          window.location.href  = "1/outcome/2"
          
        } else if (op == "Corre o mais rápido possível") {

          window.location.href  = "1/outcome/1"
        }

        else if (op == "Se finge de morto"){
          
          window.location.href  = "1/outcome/3"
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

  margin-left: 0%;

}

.rbox2{

  margin-left: -5.1%;

}

.rbox3{

  margin-left: -3.9%;

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