<template>
<v-card
    tile
    style="height: 100vh;"
    color="#1D1D1D"
    elevation="0" 
    class="pt-7 d-flex justify-start align-center cardWelcome"
>
    <div class="homeText white--text" style="width: 100%;">
        <div class="welcomeText ">
            <div>Hi,</div>
            <div> I'm Sharon, </div>
            <div> web developer</div>
        </div>
        <div class="developerText">
            Frontend developer | Backend developer
        </div>
        <div class="bubbles">
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
            <div class="bubble"></div>
        </div>
    </div>
    
</v-card>
</template>

<script>
  export default {
    name: 'Welcome',

    components: {
      
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;600&display=swap');
.cardWelcome{
  overflow: hidden;
}
.homeText{
    font-family: 'Raleway', sans-serif !important;
}
.welcomeText{
  font-size: calc(2em + 2vw) !important;
  font-weight: 700 !important;
  margin: 0 5rem !important;
}
.developerText{
  margin: 1rem 5rem 0 !important;
}
.bubble{
  border-radius:50%;
  opacity: .3;
  position: absolute;
  bottom: 100vh;
  animation: bubbleAnimation 3s linear infinite;

}

.bubble:nth-child(1){
  background: rgb(115, 56, 226);
  width: 80px;
  height: 80px;
  left: 5%;
  animation-duration: 3s;
  animation-delay:3s;
}

.bubble:nth-child(2){
  background: rgb(70, 159, 241);
  width: 100px;
  height: 100px;
  left: 35%;
  animation-duration: 3s;
  animation-delay:5s;
}

.bubble:nth-child(3){
  background: rgb(70, 159, 241);
  width: 20px;
  height: 20px;
  left: 15%;
  animation-duration: 1.5s;
  animation-delay:7s;
}

.bubble:nth-child(4){
  background: rgb(115, 56, 226);
  width: 50px;
  height: 50px;
  left: 90%;
  animation-duration: 6s;
  animation-delay:3s;
}

.bubble:nth-child(5){
  background: rgb(115, 56, 226);
  width: 70px;
  height: 70px;
  left: 65%;
  animation-duration: 3s;
  animation-delay:1s;
}

.bubble:nth-child(6){
  background: rgb(70, 159, 241);
  width: 90px;
  height: 90px;
  left: 55%;
  animation-duration: 4s;
  animation-delay:3s;
}

.bubble:nth-child(7){
  background: rgb(115, 56, 226);
  width: 30px;
  height: 30px;
  left: 72%;
  animation-duration: 5s;
  animation-delay:5s;
}
.bubble:nth-child(8){
  background: rgb(70, 159, 241);
  width: 20px;
  height: 20px;
  left: 50%;
  animation-duration: 4s;
  animation-delay:5s;
}

.bubble:nth-child(6){
  background: rgb(70, 159, 241);
  width: 90px;
  height: 90px;
  left: 25%;
  animation-duration: 4s;
  animation-delay:0s;
}

.bubble:nth-child(7){
  background: rgb(115, 56, 226);
  width: 30px;
  height: 30px;
  left: 72%;
  animation-duration: 2s;
  animation-delay:0s;
}
.bubble:nth-child(8){
  background: rgb(70, 159, 241);
  width: 20px;
  height: 20px;
  left: 50%;
  animation-duration: 6s;
  animation-delay:0s;
}

@keyframes bubbleAnimation{
  0%{
    bottom: 0;
    opacity: 0;
  }
  30%{
    transform: translateX(30px);
  }
  50%{
    opacity: .3;
  }
  100%{
    bottom:100vh;
    opacity: 0;
  }
}
@media only screen and (max-width: 452px) {
    .welcomeText{
        margin: 0 2rem !important;
    }
    .developerText{
    margin: 1rem 2rem 0 !important;
    }
}
</style>