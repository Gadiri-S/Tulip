<template>
<div class="hero-container"> 
  <Navbar/>

  <div class="header-t">
    


<div class="content">
<div class="text">
    <h3>PURE INNOVATIONS</h3>

<p>At Tulip Industries Ltd, we take pride in manufacturing disruptive technologies in Africa.</p>
</div>

<div class="button-header">
  <button>Get to know us</button>
</div>
</div>
<div class="kiosk"><!--<img src="../assets/kiosk2.png" alt="" class="kiosk-picture">--></div>


  </div>
  </div>
</template>

<script>
import Navbar from './Navbar.vue';
export default {
    name: "Header",
    components: { Navbar }
}
</script>

<style lang="scss" scoped>

.kiosk{
  width:50% ;
  height: 50vh;
  background: url('../assets/kiosk2.png');
background-size: contain;
 background-repeat: no-repeat;

 .kiosk-picture{
  width:100%;
 }
}

.hero-container{
  //background: rgb(3,0,215);
//background: linear-gradient(270deg, rgba(3,0,215,1) 8%, rgba(99,0,167,1) 100%);
background:linear-gradient(rgba(0,0,0,0.20),rgba(0,0,0,0.20)),url('../assets/bp.jpg') ;
    background-position: bottom;
    background-repeat: no-repeat;
    background-size: cover;
    

}
.header-t{
  display: flex;
  align-items: center;
    min-height: 100vh;
    padding: 0;
    margin:0;

}

.content{
    color:rgb(255, 255, 255);;
    text-align: left;
    width: 50%;
    margin-left: 5%;
 
 .text{

    h3{
        //padding-top: 10%;
        font-size: 50px;
         letter-spacing: 15px;
        margin-bottom: 20px;
    }

    p{
        font-size: 16px;
    }
 }
}

.button-header{
    margin-top: 10%;

    button{
    padding: 15px;
    font-size: 23px;
    font-weight: 600;
    border-radius: 30px;
    border:1px solid white;
font-family: 'Roboto', sans-serif;

//background:  rgb(224, 230, 227);
background:  transparent;
color: white;
transition: .4s;

&:hover{
    cursor: pointer;
   // color:#0372d8;;
   background: #0060e7;
    transition: .4s;
   border: 1px solid transparent;
   
}
    }
}





@media (max-width:1280px) {
   .header-t{
    display: flex;
    flex-direction: column;
 }
 .content{
    text-align: center;
    width: auto;
    margin: 10% 0 5% 0;

}
  .kiosk{
    height: 500px;
  }
}

@media (max-width:1000px) {
   .kiosk-picture{
  width:300px;
 }
  
}


@media (max-width:850px) {
  .header-t{
  display:flex;
  flex-direction: column;
  justify-content: center;
 width: 100%;
 text-align: center;

}

.content{
    color:rgba(255, 255, 255, 0.819);;
    text-align: center;
    width: 90%;
    margin-left: 0;
 
 .text{

    h3{
        padding-top: 20%;
        font-size: 40px;
         letter-spacing: 10px;
        margin-bottom: 20px;
        text-align: center;
    }

    p{
        font-size: 15px;
    }
 }
}

.button-header{
    margin-top: 10%;

    button{
    padding: 15px;
    font-size: 23px;
    margin: auto;


    }
}


.kiosk{
  width: 100%;
}

.kiosk-picture{

  max-width: 100%;
}

  
}
</style>