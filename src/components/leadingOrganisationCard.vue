<script>

export default {
    name:'leadingOrganisationCard',
    methods:{
        getImgUrl(imgName){
            return new URL(`../assets/${imgName}`, import.meta.url).href
        }
    },
    props:{
        cardData: Object,
    }
}
</script>

<template>
     <div class="org-card col-4 text-start filter-primary">
        <div class="top mb-3">
            <div class="img-wrapper mb-3 filter-targhet">
                <div class=""></div>
                <img class="" :src="getImgUrl(cardData.imgName)" alt="">
            </div>
            <h3 class="mb-4">{{cardData.imgText}}</h3>
        </div>
        <div class="bottom">
            <h2>{{cardData.bottomHighligh}}</h2>
            <p>{{cardData.bottomText}}</p>
        </div>
     </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/filter-primary.scss' as *;
.top{
    border-bottom: 1px dotted gray;
    height: 625px;
    overflow: hidden;
    h3{
        font-size: 32px;
    }
    .img-wrapper{
        position: relative;

    }
}
.bottom{
    p{
        font-size: 1.2rem;
    }
}

</style>