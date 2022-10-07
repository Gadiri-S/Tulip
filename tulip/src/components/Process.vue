<template>
  <div class="process-cont">

<h1>OUR PROCESS</h1>
<div class="container-process">

    <div class="process">
      
        <div class="pp"><img src="../assets/probe.png" alt="" class="picture-process fade"></div>
        <div class="process-text fade">
          <h2>Consulting and Probe</h2>
          <p>This is where we sit down, grab a cup of coffee and dial in the details. Understanding the task at hand and ironing out the wrinkles is key.<br>We pride ourselves in working closely with our clients, taking their idea or concept and developing it further.<br><br>Our Marketing and Distribution teams approach your business with care, keeping your End-Clients in mind from the initial consultation. <br>We provide not only terminals, rather, digital solutions to your employees' HR requests, and customers' sales &amp; service needs.</p>
</div>
    </div>


     <div class="process">
      
        <div class="process-text fade">
          <h2>3D CAD Design</h2>

          <p>Now that we have aligned the details, it is time to get things mapped out and organized. This part is really crucial in keeping the project in line to completion.<br>At Tulip Industries we have a passion for good engineering design. We pride ourselves in working closely with our clients, taking their idea or concept and developing it further. </p>
</div>
        <div class="pp"><img src="../assets/design.png" alt="" class="picture-process fade"></div>

    </div>
    

    <div class="process">
      
        <div class="pp"><img src="../assets/line.png" alt="" class="picture-process fade"></div>
        <div class="process-text fade">
          <h2>Precision Manufacturing</h2>

          <p>The time has come to bring those ideas and plans to life. This is where our pre approved CAD visualization gets into manufacturing by our local production plant. <br><br>We precision manufacture interactive kiosks to your specifications. </p>
</div>
    </div>


     <div class="process">
      
        <div class="process-text fade">
          <h2>Customer Support</h2>

          <p>We manage all your kiosks from one central location. With consumer autonomy on the rise, companies can streamline customer services, Real-time update contents, reduce operational costs, offer flexible and specialized services.<br><br></p>
</div>
        <div class="pp"><img src="../assets/support.png" alt="" class="picture-process fade"></div>

    </div>
     

   </div>
   
   <div class="phone">
    <img src="../assets/arrowdown.png" class="arrow-up" alt="">       

</div>
  </div>
</template>

<script>
import Header from './Navbar.vue';

import Footer from './Footer.vue'
export default {
name:'Process',
  components: {
 
},
data(){
  return {

  }
},

mounted() { 
this.fadeInElements = Array.from(document.getElementsByClassName('fade'));
document.addEventListener('scroll', this.handleScroll)

},

destroyed() { 
  document.removeEventListener('scroll', this.handleScroll)

},
methods:{

  isElemVisible(el) {
    const rect = el.getBoundingClientRect()
    const elemTop = rect.top + 200 // buffer
    const elemBottom = rect.bottom
    return elemTop < window.innerHeight && elemBottom >= 0
},
  handleScroll() {
    for (let i = 0; i < this.fadeInElements.length; i++) {
    const elem = this.fadeInElements[i]
    if (this.isElemVisible(elem)) {
        elem.style.opacity = '1'
        elem.style.transform = 'scale(1)'
        this.fadeInElements.splice(i, 1) // Pour jouer l'animation seulement une fois
    }
}
}
 

}
}
</script>

<style lang="scss" scoped>

.phone {
    position: fixed;
    text-align: right;
    top: 85%;
    left: 90%;
    margin-left: 10px;
    cursor: pointer;
}
.arrow-up{
    height: 40px;
    background: rgb(0, 113, 212);
    rotate: 180deg;
    border-radius: 50%;
    padding: 15px;
-webkit-box-shadow: 0px 5px 18px 1px rgba(0,0,0,0.4); 
box-shadow: 0px 5px 18px 1px rgba(0,0,0,0.4);
}


.process-cont{

 
        color: black;
  h1{
 
    color: black;
    font-size:60px;
  }



}
h2{
    font-size: 40px;
  color: black;
  margin: 15px 0 15px 0;
  text-align: center;
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
  justify-content: center;
    margin: 25px auto 25px auto;
   ;

}
.pp{
  width: 40%;
}
.process-text{
  width: 30%;
  text-align: left;
  margin-left: 15px;
  font-size: 20px;
  line-height: 1.5;
  border-radius: 15px;
  padding: 15px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;}
.picture-process{
    width: 100%;
    height: 100%;

}


.fade {
  opacity: 0;  
	transition: 0.3s all ease-out;  
	transform: scale(0.8);  
	box-sizing: border-box;  }

@keyframes moveright {

0% {
    transform: translateX(500px);
}
100% {
    transform: translateX(0px);

}
}

@media (max-width:1400px) {

  h2{
    font-size: 20px;
  }
  .process-text{
    font-size: 17px;

  }
  .picture-process{
    height: auto;
  }
}
@media (max-width:850px) {
  .process-cont{

  h1{
 
    color: black;
    font-size:35px;
margin:5% 0 ;
  }

  h2{
    font-size: 30px;
  color: black;
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
  margin: 20px 0 20px 0;
  font-size: 15px;
  line-height: 1.5;
}
.picture-process{
    width: 100%;
    height: 100%;

}

}

</style>