<template>
  <div>

    <div class="container-products">
        <h1>PRODUCTS AND SOLUTIONS</h1>

<div class="products">
     <div class="product"><span class="intra">Terminals and Kiosks</span><img src="../assets/599.png" alt="" class="product-img"></div>
     <div class="product"><span class="intra">Farming Assistance</span><img src="../assets/farm2.png" alt="" class="product-img"></div>
    <div class="product"><span class="intra">Softwares</span><img src="../assets/software.png" alt="" class="product-img"></div>
        <div class="product"><span class="intra">Digital Assistance</span><img src="../assets/education.png" alt="" class="product-img"></div>


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
  left: 20%;
  right:20%;
  min-width: 50%;
  color:white;
  font-size: 25px;
  font-weight: 700;
  padding: 10px;
  border-radius: 30px;
  background: #0060e7;

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
  background: url('../assets/yellow.jpg');
  background-position:left;
       background-size: cover;
        background-repeat: no-repeat;/**/

       
     
 h1 {
   color: black;
    font-size:60px;
padding:5% 0 ;
}

.product:nth-child(2n) {
border-radius: 15px;
  //border-radius:  40% 0  40% 0;
}
  .product{
  position: relative;
  text-align: center;
  background: url('../assets/6.jpg');
  background-position:left;
       background-size: cover;
        background-repeat: no-repeat;/**/

        margin: 15px;
        border-radius: 15px;
        box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;   
         .product-img{
height: 50vh;
width: 30vw;
margin: 0 25px;
object-fit: contain;
        &:hover{
          
                cursor:pointer;


        }
    }
  }
}

@media (max-width:1400px) {
  .intra {

  font-size: 20px;

}
}

@media (max-width:1000px) {

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
  width: 80vw;
  margin: 20px auto 20px auto;

    .product-img{
height: 60vh;
width: 80vw;
    
    }
  }
}
}

</style>