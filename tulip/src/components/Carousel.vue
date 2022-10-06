<template>
   <div class="carousel" data-carousel>



<i class="fas fa-angle-left carousel-button prev" data-carousel-button="prev"></i>

<i class="fas fa-angle-right carousel-button next" data-carousel-button="next"></i>



<ul data-slides>
  <li  class="slide" data-active>
    <img src="../assets/keita.jpg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/cardiology.jpg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/ultrasound.jpeg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/thermography.jpeg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/telemed.jpg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/tenor3.jpg" alt="" class="img-product">
  </li>
  <li  class="slide">
    <img src="../assets/team.jpg" alt="" class="img-product">
  </li>

  
</ul>



</div>
</template>

<script>
export default {
name:'Carousel',
data() {
    return {

    }
},
mounted(){
    this.carousel()

},

methods:{

  
    carousel(){

        const buttons = document.querySelectorAll('[data-carousel-button]')


        buttons.forEach(button => {
        
 button.addEventListener("click",()=>{ 
                    const offset = button.dataset.carouselButton === 'next'? 1 : -1;
                    const slides = button.closest("[data-carousel]")
                    .querySelector("[data-slides]");
                  


                    const activeSlide = slides.querySelector("[data-active]")

                    let newIndex = [...slides.children].indexOf(activeSlide)+offset ;
                   
                   if(newIndex<0) {newIndex = (slides.children.length) -1};
                    
                    
                    if(newIndex >=slides.children.length){newIndex = 0;} 
                    
                    slides.children[newIndex].dataset.active = true;
                    delete activeSlide.dataset.active;
                })
                   
        });
    }
},
}
</script>

<style>

    .carousel{
        background: url('../assets/shape.jpg');
       
       background-position:center;
       background-size: cover;
        background-repeat: no-repeat;    }
   .img-product{
        height: 450px;
        width:400px;
        object-fit: cover;
    }
    .slide{
    inset: 0;
        display: none;
    }
    .slide[data-active]{
  
display: block;    
}
    .carousel-button{
     position:relative;
     top: 200px;
        font-size: 30px;
        cursor: pointer;
        color: white;
    }
    .next{
        position: relative;
        left: 220px;
    }
    .prev {
        position: relative;
        right: 220px;
    }
</style>