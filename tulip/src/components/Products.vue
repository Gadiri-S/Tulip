<template>
  <div>

    <div class="container-products">
        <h1>PRODUCTS AND SOLUTIONS</h1>

<div class="products">
     <div class="product"><span class="intra">Terminals and Kiosks</span><img src="../assets/599.png" alt="" class="product-img"></div>
     <div class="product"><span class="intra">Farming Assistance</span><img src="../assets/farm2.png" alt="" class="product-img"></div>
    <div class="product"><span class="intra">Softwares</span><img src="../assets/code2.png" alt="" class="product-img"></div>
        <div class="product"><span class="intra">Digital Assistance</span><img src="../assets/school.png" alt="" class="product-img"></div>


</div>

    </div>

  </div>
</template>

<script>
export default {
name:'Products'
}
</script>

<style lang="scss">

.intra {
   position: absolute;
  top: 80%;
  left: 25%;
  right:25%;
  min-width: 60%;
  color: white;
  font-size: 25px;
  padding: 15px;
  border-radius: 30px;
 background: rgb(255, 187, 0);

z-index: 2;
                transform: scale(1); 
                transition: .3s;


&:hover{
  transition: .3s;
  cursor:pointer;
  background: rgb(255, 255, 255);
  color:rgb(48, 225, 136) ;
}



}
.products{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
}

.container-products{
  background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(65,13,255,1) 100%);


       
       background-position:left;
       background-size: cover;
        background-repeat: no-repeat;/**/
 h1 {
   color: rgb(255, 255, 255);
    font-size:60px;
padding:5% 0 ;
}

  .product{
  position: relative;
  text-align: center;

    .product-img{
height: auto;
width: 600px;
        &:hover{
          
                cursor:pointer;


        }
    }
  }
}

@media (max-width:850px) {

  .intra{
    font-size: 20px;
    width: 60%;
    min-width:60%;
    left: 0;
    right: 0;
    margin:auto;
  }
  
  .products{
    display: block;
}

.container-products{
 h1 {
    font-size:35px;
}

  .product{
  position: relative;
  text-align: center;

    .product-img{
height: auto;
width: 100%;
    
    }
  }
}
}

</style>