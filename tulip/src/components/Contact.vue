<template>
  <div class="contact">

            <h1>CONTACT</h1>


<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3933.141047952003!2d-13.560829285291065!3d9.668987493078573!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x4c6acb962fc85e2a!2s6CX8MC9R%2BHGX!5e0!3m2!1sfr!2sfr!4v1660670315333!5m2!1sfr!2sfr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
   

   <div class="fr">
  
   
   <div class="form-container">
        <form action="">
            <input type="text" placeholder="Your name*" required class="first-row">
            <input type="email" placeholder="Your email*" required class="first-row">
            <input type="text" placeholder="Object" class="second-row">
            <input type="text" placeholder="Company name (optional)" class="second-row">
            <textarea name="message" id="" cols="30" rows="10" class="message" placeholder="Message*"></textarea>
            <button class="button-send">Send Message</button>

        </form>
    </div>
    
    </div>
  </div>
</template>

<script>
export default {
name:"Contact"
}
</script>

<style lang="scss">

.contact{
    background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(65,13,255,1) 100%);


       
background-position:left;
background-size: cover;
 background-repeat: no-repeat;/**/
        h1 {
            
            color: white;
    font-size:60px;
padding:5% 0 ;
}
}

iframe{
    width: 100%;
}


.form-container{
    width: 60%;
    margin: auto;


}

.fr{
    display: flex;
}
::placeholder {
    color: white;
}
form{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    color: white;

    input{
        height: 15px;
        padding: 15px;
        margin: 15px 0 15px 0;
            border-radius: 5px;
            border: 1px solid rgb(181, 178, 178);
            font-size: 20px;
font-family: 'Roboto', sans-serif;
background: transparent;



    }
}
.first-row{
    width: 45%;
}
.second-row{
    width: 100%;
}

.message{
    width: 100%;
    margin: 20px 0 20px 0;
    padding: 15px;
    border-radius: 5px;
      border: 1px solid rgb(181, 178, 178);
            font-size: 20px;
font-family: 'Roboto', sans-serif;
background: transparent;
}

.button-send{
    border: none;
    height: 50px;
    width: 170px;
    color:white;
background: rgb(48, 225, 136);
font-size: 20px;
margin: 15px auto 15px auto;
border-radius: 30px;
   transition: .3s ease-in-out;
                transform: scale(1); 

&:hover{
                transform: scale(1.10); 
                  transition: .3s ease-in-out;
                       background: #00de6b;


                cursor:pointer;
}
}

@media (max-width:850px) {
    .form-container {
        width:100%;
        margin: 10px;

        .first-row,.second-row{
            width: 100%;
        }
    }

    .contact{
        h1{
            font-size: 35px;
        }
    }
}
</style>