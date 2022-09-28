<template>
<div> 
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
<div class="kiosk"><img src="../assets/kiosk2.png" alt="" class="kiosk-picture"></div>


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
  width:40% ;

 .kiosk-picture{
  width:100%;
 }
}
.header-t{
  display: flex;
  align-items: center;
background: linear-gradient(209deg, rgb(0, 125, 203) 24%, rgb(149, 0, 203) 87%);
       
    background-position:center;
    background-size: cover;
     background-repeat: no-repeat;
    min-height: 100vh;
    padding: 0;
    margin:0;
}

.content{
    color:rgba(255, 255, 255, 0.819);;
    text-align: left;
    width: 50%;
    margin-left: 5%;
 
 .text{

    h3{
        padding-top: 20%;
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
    border:none;
font-family: 'Roboto', sans-serif;
background: #0372d8;
color: white;
transition: .4s;

&:hover{
    cursor: pointer;
    color:#0372d8;;
    background: #ffffff;
    transition: .4s;
   /* background: transparent;
    color: white;
    transition: .4s;
    border: 1px solid #00278c;*/
}
    }
}





@media (max-width:1200px) {
   .kiosk-picture{
  width:400px;
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