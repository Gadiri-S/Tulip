<template>
<div class="container" id="container">

   <div class="header-phone"> 


                                <div class="container-icons-header">
                            <div> <router-link to="/"><img src="../assets/logo.png" alt="" class="logo"></router-link></div>
                            <div v-if="show==false" @click="showMenu"><img src="../assets/burgerwhite.png" class="icon-mobile" alt=""></div>
                            <div v-else><img src="../assets/close.png" alt="" class="icon-mobile" @click="showMenu"></div>

                            </div>

                              <div class="menu-mobile-container">
                            <div v-if="show == true">           

          <router-link to="/"><li>Home</li></router-link>
          <a @click="nav(process[0].id)"> <li>Who we are</li></a>
          <a @click="nav(process[0].id)"> <li>Our Process</li></a>
          <a @click="nav(products[0].id)"> <li>Products and Services</li></a>
            <a  @click="nav(contact[0].id)"><li>Contact us</li></a>
             </div>
                          </div>
</div>

<div class="navbar">
<div class="logo-container">
  <div> <router-link to="/"><img src="../assets/logo.png" alt="" class="logo"></router-link></div>
</div>
  <ul class="nav">

 
    <a @click="nav(process[0].id)"> <li>Our Mission</li></a>


   <div class="dropdown">
<a @click="nav(process[0].id)"> <li class="dropbtn">Our Process<i class="fas fa-angle-down arrow"></i></li></a>
  <div class="dropdown-content">
    <a>Consulting and Probe</a>
        <a>3D CAD Design</a>
    <a>Precision Manufacturing</a>
    <a>Customer Support </a>
  </div>
</div>
   
     <div class="dropdown">
<a @click="nav(products[0].id)"> <li class="dropbtn">Products and Services<i class="fas fa-angle-down arrow"></i></li></a>
  <div class="dropdown-content">
  <router-link to="/products"> Terminal & Kiosks</router-link>
    <a >Farming Assistance</a>
    <a >Softwares</a>
    <a >Digital Assistance</a>
  </div>
</div>

<li @click="nav(contact[0].id)">Contact us</li>

</ul>
</div>
</div>
</template>

<script>
export default {
name:"Navbar",

data(){
  return {
    show:false,
    contact: [
   {
id: 'contact'}],
 products: [
   {
id: 'products'}],
 process: [
   {
id: 'process'}],
home: [
   {
id: 'header'}],

  }
}, mounted() {
                                this.changeColor()

        },
methods:{
  showMenu(){
    this.show =!this.show
  },
      changeColor(){

                const header = document.getElementById('container');

                console.log(header)

document.addEventListener('scroll', function() {
  
  // Get the scroll position
  let scrollPos = window.pageYOffset;
  
  if ( scrollPos < 95 ) {
    header.style.backgroundColor = "transparent";
  } else {
    header.style.backgroundColor = "#0372d8";

    
  }
  
  
})},
 nav(id) {

        const position = document.getElementById(id).offsetTop;
          // smooth scroll
         window.scrollTo({ top: position, behavior: "smooth" });  
    }
}
}
</script>

<style lang="scss">

 

.header-phone{
  display: none;
}

.container{
 // position: fixed;
 background: transparent;
  width:100%;
       z-index: 999;
       

}
.dropbtn{
    display: flex;
    align-items: flex-end;

    .arrow{
        color: white;
        font-size: 15px;
        margin-left: 10px;
      transform: rotate(0deg);
            transition: .4s ease-in-out;
        

    }
}

/* The container <div> - needed to position the dropdown content */
.dropdown {
  position: relative;
  display: inline-block;
}

/* Dropdown Content (Hidden by Default) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: black;
  border-radius: 15px;
  min-width: 400px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
  margin-top: 10px;
}

/* Links inside the dropdown */
.dropdown-content a {
  color: white;
 padding: 12px 16px;
  text-decoration: none;
  display: block;
  border-left: 7px solid transparent;
  text-align: left;
  &:hover{
    cursor: pointer;
  }
}

/* Change color of dropdown links on hover */
.dropdown-content a:hover {background-color: rgba(45, 36, 36, 0.207);  border-left: 7px solid #00ade7;


}

/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {display: block;}

/* Change the background color of the dropdown button when the dropdown content is shown */
.dropdown:hover .dropbtn { color:rgba(255, 255, 255, 0.819);;


.arrow{
  color:rgba(255, 255, 255, 0.819);;
      transform: rotate(180deg);
            transition: .4s ease-in-out;

}
}


.navbar {
    display: flex;
    justify-content: space-around;
        padding: 2% 5% 2% 5%;
        height: 50px;
        /*Don't align center or the menu won't display*/



  
}



    .dropdown-content:hover{
            display: block;
        }

.nav{
    display: flex;
    justify-content: space-around;
          /* color: rgba(255,255,255,0.5);*/
          color: white;
           font-size: 20px;

        
           
           

           li{
            list-style:none;           
            margin: 5px 10px;
            cursor: pointer;
              //font-weight: 600;


            &:hover{
              color:rgba(255, 255, 255, 0.819);;
            }
           }



}

.logo{
    height: 120px;
    cursor: pointer;
    position:relative;
    bottom: 30px;
}


.logo-container{
  padding: 0;
  margin: 0;
}
 @keyframes moveup {

        0% {
            transform: translateY(-400px);
        }
        100% {
            transform: translateY(0px);
    
        }}
           @keyframes moveright {

        0% {
            transform: translateX(500px);
        }
        100% {
            transform: translateX(0px);
    
        }
    }


a{
text-decoration: none;

&:visited{
  color:inherit;
}
}

@media (max-width:1200px) {

  

  .container-icons-header{
    display: flex;
    justify-content: space-around;
    padding: 5%;
  }

  .navbar{display: none;}

  .header-phone{

     
display: block;

.menu-mobile-container{
    text-align: left;

   a li{
    background: white;
    list-style: none;
    padding: 5px 0 5px 25px;
    font-size: 25px;
    border-bottom: 1px solid gainsboro;

    &:hover{
      background: #e5e5e5;
      cursor: pointer;
    }
    }
    }
  }
  
  .icon-mobile{
    height: 50px;
    cursor: pointer;
  }
}
</style>