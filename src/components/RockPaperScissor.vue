<template>
<section>
<div v-if="isStart">
        <button @click="user = 'rock'; getComputerChoice()">Rock</button>
        <button @click="user = 'paper'; getComputerChoice()">Paper</button>
        <button @click="user = 'scissors'; getComputerChoice()">Scissor</button>

        Vs

      {{ computer ? computer : 'Computer'}}
      <br>
    <div v-if="user != '' && computer != ''">
      {{determineWinner()}}
    </div>
    
  </div>
  <div v-else>
    <button @click="isStart = !isStart"><strong>Start Game Here</strong></button>
  </div></section>
</template>


<script>

export default {
    name: 'RockPaperScissor',


        data () {
            return {
                user: '',
                computer: '',
                isStart: false
            }
        },
       
        methods: {
            startGame(){

            },

        determineWinner(){
                const userChoice = this.user;
                const getComputerChoice = this.computer;
                if ( userChoice === 'rock'){
                    if(getComputerChoice === "paper"){
                        return "computer won";
                    } else {
                        return "user won";
                    }
                }

            if (userChoice === "paper"){
                if (getComputerChoice === "scissors"){
                    return "computer won";
                } else {
                    return "user won";
                }
            }
            if (userChoice ==="scissors"){
                if (getComputerChoice === "rock"){
                    return "computer won";
                }
                else {
                    return "user won";
                }
            }
            if (userChoice ==="rock"){
                if (getComputerChoice === "rock"){
                    return "Its a tie";
                }
            }
             if (userChoice ==="paper"){
                if (getComputerChoice === "paer"){
                    return "Its a tie";
                }
            }
             if (userChoice ==="scissors"){
                if (getComputerChoice === "rock"){
                    return "Its a tie";
                }
            }
        },
            getComputerChoice(){
                const randomNumber = Math.floor(Math.random()* 3)
                if (randomNumber === 0){
                    this.computer = "rock";
                }
                else if (randomNumber ===1){
                    this.computer = "paper";
                } else {
                    this.computer = "scissors";
                }
            }
            
        }
};
</script>
