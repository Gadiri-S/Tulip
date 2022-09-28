<template>
  <div class="presentation-container">

<div class="intro">
  <h1>Who we are and what we do</h1>
  <p>Tulip Industries Headquarters, located in Guinea, offer a convenient and affordable way to fully access the Internet,and other digital contents and or services to the public. Our work stations provide full access to the Web,  the emails, scanners, printers, educational and professional applications. Tulip Industries provide communities with 
    unique and innovative products and services. Our secured public kiosks appeal to individuals of all ages and backgrounds.
    The ease-of-use and instructional menu makes it easy to use for an audience that does not associate themselves with the
    computer age. Various locations, such as schools, sidewalks, hotels and restaurants, administrative buildings etc. will
     provide customers and users with a convenient way to access the Internet and digital contents away from the office and home.</p>

    </div>
<div class="pic-container"><img src="../assets/keita.jpg" alt="" class="presentation-picture"></div>

  </div>
</template>

<script>
export default {
name:'Presentation'
}
</script>

<style lang="scss">
.presentation-container{
  display: flex;
  height: auto;

  h1{
    margin: 15px 0;
  }
}
.intro {
  font-size: 20px;
  line-height: 1.5;
  color: rgb(16, 0, 39);
  text-align: left;
  margin: 15px;
  width: 50%;
}

.pic-container {
  width:50%;
}
.presentation-picture {
  width: 100%;
  height: 500px;
  object-fit: cover;
}


@media (max-width:850px) {

  .presentation-container{
  display: flex;
  flex-direction: column;
  justify-content: center;

  h1{
    margin: auto;
    text-align: center;
  }
}
.intro {
  font-size: 17px;
  line-height: 1.5;
  color: rgb(16, 0, 39);
  text-align: left;
  margin:  10px;
  width: 90%;
}

.pic-container {
  width:100%;
}
.presentation-picture {
  width: 100%;
  height: 500px;
  object-fit: contain;
}

  
}
</style>