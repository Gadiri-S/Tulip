<template>
  <div class="container-products">
    <Navbar/>

    <div class="content">
        <h1>Telemedicine</h1>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
export default {
    components: { Navbar }
}
</script>

<style lang="scss" scoped>

    .container-products{
        min-height: 100vh;
        background: linear-gradient(209deg, rgb(0, 125, 203) 24%, rgb(149, 0, 203) 87%);

    }

    .content{
        padding-top: 15vh;

        h1{
            color: white;
        }
    }

</style>