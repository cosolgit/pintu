<template>
  <div id="app">
    <d-puzzle v-bind="puzzleConfig[level]" @next="handleNext"/>
  </div>
</template>

<script>
  import DPuzzle from './Puzzle'
  export default {
    components:{
      DPuzzle
    },
      data(){
        return{
            level:0,
            puzzleConfig:[
              {row:2,col:2,img:'../puzzleimg/4.png'},
              {row:3,col:3,img:'../puzzleimg/4.png'},
            ]
        }
      },
      methods:{
          handleNext(){
            if(++this.level==this.puzzleConfig.length){
             const answerFlag= window.confirm('已经是最后一关了,重新开始吗');
             if(answerFlag){
               this.level=0;
             }
            }

          }
      }
  }
</script>
<style lang="scss">
*{
  margin:0;
  padding:0
}
</style>
