<template>

  <section class="container">
    <div center>
      <h1 class="title">
        Placar de Futebol 
        </h1>
        <h2 class="subtitle">Faça suas apostas</h2>
      <form> 
        TIME <br> <input type="text" v-model="cxtime1" class="caixadetexto" size="15"><br>
        TIME <br> <input type="text" v-model="cxtime2" class="caixadetexto" size="15"><br>
        <div v-on:click="Jogar()" value="jogar" size="15" class="button--green">jogar </div>
        
        
        
      </form> 
      
      
        <table> 
          <tr>
          <th>TIMES</th> <th>RESULTADO</th>
        </tr>
<tr>
        <input id="result" v-model="time1"/>
          <td id="resultado1" >Placar1</td>
</tr>
<tr>
      <input  id="result2" v-model="time2"/>
      <td id="resultado2">Placar2</td>
</tr>
</table>
      
    </div>
  </section>
</template>

<script>

import AppLogo from '~/components/AppLogo.vue'

export default {
  
        
  data (){
    
    return {
     cxtime1:  '',
     cxtime2:  '',
     time1:  '',
     time2:  '',
    

     }  
     

  },
  methods: {
      Jogar(){

            let alterar = this.cxtime1;
            this.time1 = alterar ;
            
            let alterar1 = this.cxtime2;
            this.time2 = alterar1;
            document.getElementById('resultado1').innerHTML= Math.floor(Math.random() * 10);
            document.getElementById('resultado2').innerHTML= Math.floor(Math.random() * 10);
     },
     
      
  }
}

</script>

<style>
.table{
  border: 1px solid black
}
.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}
.caixadetexto{
  border-radius: 2%;
}

.placar{
  text-align: center;
  font-family: 'Courier New', Courier, monospace;
  color: #f1f1f1;


}

.container {
  min-height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 5px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

