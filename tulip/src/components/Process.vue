<template>
  <div class="process-cont">

<h1>OUR PROCESS</h1>
<div class="container-process">

  <h2>Consulting and Probe</h2>

    <div class="process">
      
        <div class="pp"><img src="../assets/probe.png" alt="" class="picture-process"></div>
        <div class="process-text"> <p>This is where we sit down, grab a cup of coffee and dial in the details. Understanding the task at hand and ironing out the wrinkles is key.<br>We pride ourselves in working closely with our clients, taking their idea or concept and developing it further.<br><br>Our Marketing and Distribution teams approach your business with care, keeping your End-Clients in mind from the initial consultation. <br>We provide not only terminals, rather, digital solutions to your employees' HR requests, and customers' sales &amp; service needs.</p>
</div>
    </div>

      <h2>3D CAD Design</h2>

     <div class="process">
      
        <div class="process-text"><p>Now that we have aligned the details, it is time to get things mapped out and organized. This part is really crucial in keeping the project in line to completion.<br>At Tulip Industries we have a passion for good engineering design. We pride ourselves in working closely with our clients, taking their idea or concept and developing it further. </p>
</div>
        <div class="pp"><img src="../assets/design.png" alt="" class="picture-process"></div>

    </div>
    
     <h2>Precision Manufacturing</h2>

    <div class="process">
      
        <div class="pp"><img src="../assets/line.png" alt="" class="picture-process"></div>
        <div class="process-text"> <p>The time has come to bring those ideas and plans to life. This is where our pre approved CAD visualization gets into manufacturing by our local production plant. <br><br>We precision manufacture interactive kiosks to your specifications. </p>
</div>
    </div>

      <h2>Customer Support</h2>

     <div class="process">
      
        <div class="process-text"><p>We manage all your kiosks from one central location. With consumer autonomy on the rise, companies can streamline customer services, Real-time update contents, reduce operational costs, offer flexible and specialized services.<br><br></p>
</div>
        <div class="pp"><img src="../assets/code2.png" alt="" class="picture-process"></div>

    </div>
     

   </div>
   

  </div>
</template>

<script>
import Header from './Navbar.vue';

import Footer from './Footer.vue'
export default {
name:'Process',
  components: {
 
}
}
</script>

<style lang="scss" scoped>

.process-cont{

  background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(65,13,255,1) 100%);
       
       background-position:center;
       background-size: cover;
        background-repeat: no-repeat;/**/
        color: white;
  h1{
 
    color: white;
    font-size:60px;
margin:5% 0 ;
  }

  h2{
    font-size: 40px;
  color: white;
  margin: 15px 0 15px 0;
  text-align: left;
  }

}


.container-process {

display: flex;
flex-wrap: wrap;
justify-content: space-around;
min-height: 100vh;
}

.process{
  display: flex;
  align-items: center;
    margin-bottom: 25px;

}
.pp{
  width: 40%;
}
.process-text{
  width: 50%;
  text-align: left;
  margin-left: 15px;
  font-size: 20px;
  line-height: 1.5;
}
.picture-process{
    width: 100%;
    height: 100%;

}

@media (max-width:850px) {
  .process-cont{

  h1{
 
    color: black;
    font-size:35px;
margin:5% 0 ;
  }

  h2{
    font-size: 40px;
  color: rgb(16, 0, 39);
  margin: 25px 0 25px 0;
  text-align: center;
  }

}


.container-process {

display: flex;
flex-direction: column;
min-height: 100vh;
}

.process{
  display: flex;
  flex-direction: column;

  align-items: center;
    margin-bottom: 25px;
    

}
.pp{
  width: 100%;
}
.process-text{
  width: 90%;
  text-align: left;
  margin-left: 5px;
  font-size: 15px;
  line-height: 1.5;
}
.picture-process{
    width: 100%;
    height: 100%;

}

}

</style>