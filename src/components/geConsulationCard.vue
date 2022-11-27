<script>
export default {
    name:'getConsulationCard',
    props:{
        cardData:Object, 
    },
    methods:{
        bg(color){
            return `bg-${color}`
        },
        getImgUrl(imgName){
            return new URL(`../assets/${imgName}`, import.meta.url).href
        }
    }
}
</script>

<template>
   
    <div class="row ">
        <div class="col-6">
            <div class="img-wrapper">
                <img :src="getImgUrl(cardData.imgName)" alt="">
            </div>
        </div>
            <div class="text col-6">
                <div class="top-feature">
                    <div class="svg" :class="bg(cardData.topBadgeBg)" v-html="cardData.topBadge"></div>
                    <span>{{cardData.topText}}</span>
                </div>
                <h2>{{cardData.title}}</h2>
                <div class="info-text">
                    <p>{{cardData.text}}</p>
                </div>
                <a href="#" class="sc-button full">{{cardData.buttonText || 'Get Consultation'}}</a>
                
            </div>
        <div class="col-6"></div>
    </div>

</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/sc-button.scss' as *;
@use '../style/partials/variables' as *;

.row > *{
    padding: 0 50px;
     margin: 50px auto;
}
    .text{
        text-align: left;
        .svg{
            width: 40px;
            display: inline-block;
            margin-right: 10px;
            aspect-ratio: 1 / 1;
            border-radius: 50%; 
            color: white;
            line-height: 40px;
            text-align: center;
        }

        .info-text{
            max-height: 140px;
            overflow: auto;
            margin-bottom: 30px;
        }

        h2{
            font-size: 3rem;
        }
        p{
            font-size: 1.5rem;
            
        }
    }


</style>