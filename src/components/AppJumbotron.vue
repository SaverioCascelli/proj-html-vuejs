<script>
import ctaCard from './ctaCard.vue';
export default {
    name:'AppJumbotron',
    components:{
        ctaCard,
    }
}
</script>

<template>
    <div class="jumbotron p-0">
        <div class="container">
            <div class="row">
                <div class="left-jumbo col-6 text-white">
                    <h1>Unlock Your Online Growth Potential</h1>
                    <h3>Online marketing to secure customer retention, lead, and sales. We focus on the bigger picture.</h3>
                    <button class="sc-button bg-white text-black">Our Servicess<i class="fa-solid fa-arrow-right"></i></button>
                </div>
            <div class="col-6 right-jumbo">
                <ctaCard
                class="jumbo-card"/>
            </div>
            </div>
        </div>
    </div> 
  
</template>

<style lang="scss" scoped>
 @use '../style/partials/sc-button.scss' as *;
 @use '../style/general.scss' as *;
.jumbotron{
    width: 100%;
    height: 693px;
    background-image: url('../assets/marketing-intro.jpg');
    background-repeat: no-repeat;
    background-size: 120%;
    background-position: 50% 0%;
    
    .left-jumbo{
        padding: 120px 0;
        & > *{
            margin-bottom:35px;
        }
        h1{
            font-size: 70px;
        }
        i{
            margin-left:6px;
        }
    }

    .right-jumbo{
        position: relative;
        .jumbo-card{
            position: absolute;
            top: 20%;
            left: 17%;
        }
    }
}

</style>