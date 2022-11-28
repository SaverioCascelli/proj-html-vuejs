<script>
import advice from '../data/advice';
export default {
    name: 'Advice',
    data(){
        return{
            advice,
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
    <div class="row">
        <div class="col-6">
            <h2>Marketing Resources: Insider Advice on How to Increase Online Sales</h2>
        </div>
    <div class="col-6 d-flex justify-content-end align-items-end">
            <a href="#" class="sc-button full">Explore All Resources</a>
        </div>
    </div>

    <div class="row cards-row ">
        <a class="col-4 filter-primary text-decoration-none text-black"
        v-for="(card,index) in advice" :key="index">
            <div class="img-wrapper filter-targhet ">
                <img  class="filter-targhet" :src="getPathImage(card.imgName)" alt="">
            </div>
            <div class="text-wrapper">
                <h3>{{card.text}}</h3>
            </div>
        </a>
    </div>
</template>
<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/sc-button.scss' as *;
@use '../style/partials/filter-primary.scss' as *;
.cards-row{
    margin-top: 90px;
}
.img-wrapper{
    margin-bottom:30px ;
}

</style>