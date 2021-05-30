<template>

    <div>

    
        <p class = "texto">  
            Você finalmente consegue ler o bilhete: “Vamos fazer parecer um acidente. Misture o
            conteúdo deste frasco na comida dele. O remédio vai começar a fazer efeito depois
            de 30 minutos. Quando ele estiver completamente apagado, leve-o até o pé da
            árvore mais alta no início da floresta e direcione a manada de búfalos em sua
            direção. Estaremos esperando no laboratório ao norte do acampamento.” O que
            você faz? &#129300;
        </p>
        
        <p class = "opcoes"> Escolha uma das opções:  </p>
        <ul>

            <input class = "rbox1" type="radio" id = "1" name = "Op"  v-model = "opcao" value = "Foge e liga para a polícia">
            <label class = "tbox" for="1" >A. Foge e liga para a polícia</label><br>
            <input class = "rbox2" type="radio" id = "2" name = "Op" v-model = "opcao" value="Amarra o homem e vai ao laboratório">
            <label class = "tbox" for="2">B. Amarra o homem e vai ao laboratório</label><br>
            <input class = "rbox3" type="radio" id = "3" name = "Op" v-model = "opcao" value = "Mata o homem, pega a marreta e vai ao laboratório">
            <label class = "tbox" for="3">C. Mata o homem, pega a marreta e vai ao laboratório</label><br>
            
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
        
        if (op == "Foge e liga para a polícia"){
        
          window.location.href  = "3/outcome/1"
          
        } else if (op == "Amarra o homem e vai ao laboratório") {

          window.location.href  = "3/outcome/2"
        }

        else if (op == "Mata o homem, pega a marreta e vai ao laboratório" ){
          
          window.location.href  = "3/outcome/3"
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

  margin-left: -12%;

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