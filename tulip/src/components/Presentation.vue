<template>
  <div class="presentation-container">

<div class="intro">
  <h1>Our mission : Technology at the service of the many</h1>
  <p>Tulip Industries Headquarters, located in Guinea, offer a convenient and affordable way to fully access the Internet,and other digital contents and or services to the public. Our work stations provide full access to the Web,  the emails, scanners, printers, educational and professional applications. Tulip Industries provide communities with 
    unique and innovative products and services. Our secured public kiosks appeal to individuals of all ages and backgrounds.
    The ease-of-use and instructional menu makes it easy to use for an audience that does not associate themselves with the
    computer age. Various locations, such as schools, sidewalks, hotels and restaurants, administrative buildings etc. will
     provide customers and users with a convenient way to access the Internet and digital contents away from the office and home.</p>

     <div class="more-button">
     <button class="more">Learn more</button></div>
    </div>
<div class="pic-container"><img src="../assets/team.jpg" alt="" class="presentation-picture"></div>

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
  min-height: 100vh;
  align-items: center;
  padding: 0 2%;


  h1{
    margin: 15px 0;
  }
}
.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 22px;
  line-height: 1.5;
  color: black;
  text-align: left;
  margin: 15px;
  width: 50%;
}

.pic-container {
  width:50%;
}
.presentation-picture {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 0 30% 0 30%;
  //box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.more-button{
  margin: 25px auto 25px auto;

}
.more{
  padding: 15px;
  font-size: 20px;
  background: #00ade7;
  color: white;
  border-radius: 25px;
  border: none;
  cursor: pointer;
}




@media (max-width:1400px) {

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
  font-size: 20px;
  line-height: 1.5;
  color: black;
  text-align: left;
  margin:  10px;
  width: 90%;
}

.pic-container {
  width:100%;
}
.presentation-picture {
  width: 100%;
  height: auto;
  object-fit: contain;
  border-radius: 25px;
}

.more-button{
  margin: 25px auto 25px auto;

}
  
}

@media (max-width:850px) {
  h1{
    font-size: 30px;
  }
  .intro{
    font-size: 17px;
  }
}
</style>