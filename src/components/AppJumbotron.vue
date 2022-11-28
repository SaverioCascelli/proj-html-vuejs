<script>
import ctaCard from './ctaCard.vue';
import { store } from '../data/store';
export default {
    name:'AppJumbotron',
    components:{
        ctaCard,
    },
    data(){
        return{
            store,
        }
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
                    <button class="sc-button">Our Servicess<i class="fa-solid fa-arrow-right"></i></button>
                </div>
                <div class="col-6 right-jumbo">
                    <ctaCard
                    class="jumbo-card"/>
                </div>
            </div>
        </div>
        <div class="info-box">
            <i class="top fa-solid fa-folder-open"></i>
            <p class="bottom">Demos</p>
        </div>
        <div class="info-box ">
            <p class="top col-magic-mint"><span>$</span>{{store.price}}</p>
            <p class="bottom">On Sale</p>
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
    position: relative;
    
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
        .sc-button{
            background:white;
            color: black;
            border: 1px solid white;
            &:hover{
                background: rgba($color: #000000, $alpha: 0);
                color: white;
            }
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

    .info-box{
        text-align: center;
        font-size: .7rem;
        width: 65px ;
        aspect-ratio: 1 / 1;
        position: absolute;
        right: 10px;
        top: 30px;
        background: white;
        border: 1px solid;
        border-radius: 10px;
        padding: 2px;
        .top{
            height: 70%;
            font-size: 1.7rem;
            padding: 5px;
            padding-left: 15px;
            line-height: 1.7rem;
            font-weight: bold;
            position: relative
            }
        span{
            font-size: 1rem;
            display: inline-block;
            position: absolute;
            top: -3px;
            left: 10px;
            
        }
        & > *{
            margin: 0;
        }
        &:last-child{
            top: 100px;
        }
     }
}

</style>