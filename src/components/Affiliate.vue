<script>
import {store} from '../data/store';
import Affiliate from '../data/affiliate'
export default {
    name:'Affiliate',
    data(){
        return{
            store,
            Affiliate
        }
    },
    methods:{
        getPathImage(imageName){
            return new URL(`../assets/${imageName}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="row top-text">
        <div class="col text-center mb-5">
            <h2>Some Brands We Work With</h2>
            <p>Lorem ipsum dolor sit amet consectetur.</p>
        </div>
    </div>
    <div class="row affiliate-list justify-content-between">
        <div class="col-auto"
        v-for="(element, index) in Affiliate" :key="index">
            <img :src="getPathImage(element.url)" :alt="element.name">
        </div>
    </div>

    <div class="row">
        <div class="col cta ">
            <div class="left">
                <div class="img-wrapper">
                    <img src="../assets/marketing-expert-cta.png" alt="">
                </div>
                <div class="text">
                    <h5>Sandy Riff</h5>
                    <p>Marketing Consultant Expert</p>

                </div>
            </div>
            <div class="center">
                <h3>Drive Leads and Sales with Avada</h3>
            </div>
            <div class="right">
                <button class="sc-button"><i class="fa-solid fa-phone pe-2"></i>{{store.phoneNumber}}</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/sc-button.scss' as *;
@use '../style/partials/variables' as *;

.top-text{
    h2{
        font-size: 45px;
    }
    p{
        font-size: 1.5rem;
    }
}

.affiliate-list{
    margin-bottom: 150px;
}
.affiliate-list img{
    width: 140px;

}
.cta{
    margin-bottom: 150px;
    padding: 0 50px;
    display: flex;
    align-items: center;
    height: 100px;
    box-shadow: 1px 1px 2px 1px grey;
    justify-content: space-between;
    border-radius: 10px;
    .left{
        display: flex;
        flex-direction: row; 
        align-items: center;
        .img-wrapper{
            width: 75px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 30px;
            img{
                object-fit: cover;
            }
        }
        .text > *{
            margin: 0px;
        }
    }
    .center{
        padding-right: 10%;
    }
}
</style>