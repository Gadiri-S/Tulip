<template>
  <div class="contact">

            <h1>CONTACT</h1>

   

   <div class="fr">
  
   
   <div class="form-container">
        <form action="">
            <input type="text" placeholder="Your name*" required class="first-row">
            <input type="email" placeholder="Your email*" required class="first-row">
            <input type="text" placeholder="Object" class="second-row">
            <input type="text" placeholder="Company name (optional)" class="second-row">
            <textarea name="message" id="" cols="15" rows="5" class="message" placeholder="Message*"></textarea>
            <button class="button-send">Send Message</button>

        
        </form>
        <div class="infos">
            <div class="socials">
                <i class="fab fa-linkedin-in"></i>
                <i class="fab fa-facebook-f"></i>
                <i class="fab fa-instagram"></i>
                <i class="fab fa-twitter"></i>
            </div>
            <div class="info-icon"><i class="fas fa-phone-alt"></i><p>+224 622 35 41 53</p>
</div>
            <div class="info-icon"><i class="fas fa-map-marker-alt"></i><p>Rond-Point route le Prince, Sonfonia gare</p></div>
            <div class="info-icon"><i class="fas fa-clock"></i> <p>Monday - Friday : 8:30am - 5:30pm</p></div>

          
           
        </div>
    </div>
    
    </div>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3933.141047952003!2d-13.560829285291065!3d9.668987493078573!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x4c6acb962fc85e2a!2s6CX8MC9R%2BHGX!5e0!3m2!1sfr!2sfr!4v1660670315333!5m2!1sfr!2sfr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

  </div>
</template>

<script>
export default {
name:"Contact"
}
</script>

<style lang="scss">

.contact{

        h1 {
            
            color: black;
    font-size:60px;
padding:2% 0 ;
}
}

iframe{
    width: 100%;
    min-height: 100vh;
}


.form-container{
   display: flex;
   justify-content: space-evenly;
   padding: 2%;
   margin:auto;


}

.fr{
    display: flex;
}
::placeholder {
    color: rgb(151, 151, 151);
}

.infos{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width:40%;
    border-radius: 15px;
    height: auto;
    background: url('../assets/purp.jpg');
background-size: cover;
 background-repeat: no-repeat;
     padding:15px;
     text-align: left;

    .info-icon{
        display: flex;
        color:white;
        margin: 5% 0 5% 0;

        p{
            font-size: 25px;
            margin-left: 15px;
        }
    }
    i{
        color: white;
        font-size:40px;
    }

    .socials{
        display: flex;
        justify-content: space-between;
        width:100%;
        margin: 5% 0 5% 0;
    }
   }
form{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    color: black;
    width: 40%;
    padding: 15px;
    border-radius:  15px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

    input{
        height: 15px;
        padding: 15px;
        margin: 15px 0 15px 0;
            border: none  ;
            border-bottom: 1px solid rgb(181, 178, 178);
            font-size: 20px;
font-family: 'Roboto', sans-serif;
background: transparent;
color: black;



    }
}
.first-row{
    width:40%;
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
color: white;
}

.button-send{
    border: none;
    height: 50px;
    width: 80%;
    color:white;
background: #0060e7;
font-size: 20px;
margin: 15px auto 15px auto;
border-radius: 15px;
   transition: .3s ease-in-out;
                transform: scale(1); 

&:hover{
                transform: scale(1.10); 
                  transition: .3s ease-in-out;
                       background: rgb(0, 220, 99);


                cursor:pointer;
}
}

@media (max-width:1000px) {


    .form-container {
        display: flex;
        flex-direction: column;
        width:100%;
        margin: 10px;


        .first-row,.second-row{
            width: 100%;
        }
    }

    .infos,form{
        width: 80%;
        margin: 25px auto;
    }

    .contact{
        h1{
            font-size: 35px;
        }
    }
}
</style>