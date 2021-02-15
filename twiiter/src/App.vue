<template>
  <div id="app">
    <NavigationBar />
    
   <button @click="start" :disabled="isPlaying"> PLAY NOW! </button>
   <Block v-if="isPlaying" :delay="delay" @end ="endGame"/>
   <Results v-if="showResults" :score="score"/>
  </div>
</template>

<script>

import NavigationBar from './components/NavigationBar'
import Block from './components/Block'
import Results from './components/Results'



export default {
  name: 'App',
  components:{
    NavigationBar,
    Block,
    Results
    },
  data(){
    return{ 
      isPlaying:false,
      delay:null,
      score:null,
      showResults:false
    }
  },
  methods:{
    start(){
      this.isPlaying = true;
      this.delay = 2000 + Math.random() * 5000;
      this.showResults = false;
      
    },
    endGame(reactionTime){
      this.score = reactionTime;
      this.isPlaying = false;
      this.showResults = true;
    }
  }

}
</script>

<style scoped>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  flex-direction:column;
  text-align: center;
}
button{
  margin-top:10%;
  width:30%;
  padding: 20px;
    
 }




</style>
