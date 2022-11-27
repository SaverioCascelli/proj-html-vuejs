<script>

export default {
    name:'awardsCard',
    props:{
        dataAward: Object,
    },
    methods:{
        getImgUrl(imgName){
            return new URL(`../assets/${imgName}`, import.meta.url).href
        }

    }

    
}
</script>

<template>
    <div class="col-auto d-flex flex-column align-items-center">
        <div class="img-wrapper">
            <img class="" style="" :src="getImgUrl(dataAward.imgName)" alt="">
        </div>
        <div class="text-wrapper">
            <p>{{dataAward.text1}}</p>
            <p>{{dataAward.text2}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/filter-primary.scss' as *;

.img-wrapper{
    width: 100px;
}

.text-wrapper{
    font-size: 1.1rem;
    p{
        margin: 0;
    }
}

</style>