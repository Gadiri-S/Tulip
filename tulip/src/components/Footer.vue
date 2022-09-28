<template>
  <div class="footer">



<div class="footer-container">
<div class="menu-footer">
  <ul>
    <li @click="nav(company[0].id)">Company</li>
    <li @click="nav(process[0].id)">Our Process</li>
    <li @click="nav(products[0].id)">Products</li>
    <li @click="nav(contact[0].id)">Contact</li>
  </ul>
</div>

<div class="address">
  <p>Rond-Point route le Prince, Sonfonia gare</p>
  <p>Commune de Ratoma, Conakry, République de Guinée</p>
  <p>Monday - Friday : 8:30am - 5:30pm</p>
  <p>Telephone : +224 622 35 41 53</p>
</div>


<div class="socials">

  <div class="icon"><a href="https://www.linkedin.com/company/tulip-industries-ltd/"><i class="fab fa-linkedin-in"></i></a></div>
    <div class="icon"><a href="https://www.facebook.com/tulipindustry"><i class="fab fa-facebook-f"></i></a>  </div>
  <div class="icon"><a href=""><i class="fab fa-instagram"></i></a></div>
    <div class="icon"><a href="https://twitter.com/tulipindustries?lang=fr"><i class="fab fa-twitter"></i></a></div>


</div>

</div>

 <a @click="nav(home[0].id)">  <img src="../assets/logo.png" alt="" class="logo-footer"></a>


  </div>
</template>

<script>
export default {
name:'Footer',

data() {
  return {
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
company: [
   {
id: 'company'}],
  }
},
methods:{
   nav(id) {

        const position = document.getElementById(id).offsetTop;
          // smooth scroll
         window.scrollTo({ top: position, behavior: "smooth" });  
    }
}
}
</script>

<style lang="scss">

.logo-footer{
      height: 150px;
      margin: 25px;
      cursor: pointer;

}
.footer{
background: black;
color: white;
}

.footer-container{
  display: flex;

  justify-content: space-evenly;
  padding-top: 50px;
}

.menu-footer{

  li{
    list-style-type: none;
    text-align: left;
    font-size: 20px;
    margin: 25px auto;

    &:hover{
      color:rgba(255, 255, 255, 0.819);;
      transition: .4s ease-in-out;
      cursor: pointer;
    }
  }

}

.address {
  font-size: 20px;
  text-align: left;

  p{
    margin:15px auto
  }

}

.socials {
  display: flex;
  font-size: 30px;

  a:visited{
  text-decoration: none;
  color: inherit;
  }


  .icon {margin: 0 20px 0 20px;
    transition: .4s ease-in-out;
                transform: scale(1); 
  &:hover{
    color:rgba(255, 255, 255, 0.819);;
      transition: .4s ease-in-out;
                transform: scale(1.10); 
    }
  }
}

@media (max-width:1000px) {
  .footer-container {
    display: flex;
    flex-direction: column;
align-items: center; 

.address{
  text-align: center;
  margin-bottom:30px;
}
}
}
</style>