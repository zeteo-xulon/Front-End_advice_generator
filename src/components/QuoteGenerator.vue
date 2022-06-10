<script>
  const server = "https://api.adviceslip.com/advice"
  export default {
    data(){ return { adviceId: "", adviceText: "" } },
    methods:{
      async getAdvice(){
        try{
          const fetchServer = await fetch(server);
          const response = await fetchServer.json();
          this.adviceId = response.slip.id;
          this.adviceText = response.slip.advice;
        }
        catch(err){ console.log(err) }
      },
      async rollDice(){ try{ await this.getAdvice() } 
      catch(err){ console.log(err) }}
    },
    beforeMount(){ this.getAdvice() }
  }
</script>


<template>
  <h1 class="advice__title">ADVICE #{{adviceId}}</h1>
  <p class="advice__text">"{{adviceText}}"</p>

  <div class="stylish__container">
    <div class="stylish__bar"></div>

      <div class="double__bar__container">
        <div class="double__bar"></div>
        <div class="double__bar"></div>
      </div>

    <div class="stylish__bar"></div>
  </div>

  <div class="dice__circle" @click="rollDice">
    <img src="../assets/images/icon-dice.svg" 
    class="advice__button" 
    id="adviceButton" 
    @click="rollDice"/>
  </div>
</template>


<style>

</style>