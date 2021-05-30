<template >

    <div class = "container">
        <div>
            <Logo />
            <h1 v-if = "slug.slug == 1" class="title">
             Primeira Fase do Game!
             </h1>

             <h1 v-if = "slug.slug == 2" class="title">
             Segunda Fase do Game!
             </h1>

             <h1 v-if = "slug.slug == 3" class="title">
             Última Fase do Game!
             </h1>


            <div class= "componentes">
    <body v-if="slug.slug == 1">
        <Etapa1/>
        <Breadcrumb nivel = 1 />
    </body>

    <body v-if="slug.slug == 2">
        <Etapa2/>
        <Breadcrumb nivel= 2 />
        
    </body>

    <body v-if="slug.slug == 3">
        <Etapa3/>
        <Breadcrumb nivel= 3 />
    </body>
    

                    </div> 
            </div> 
    </div> 

  

</template>



<script>



export default {

       
    
    data(){
        return {
            slug : this.$route.params

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
  padding-top: 15px;
}


</style>