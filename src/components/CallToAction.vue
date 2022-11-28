<script>
import ctaCard from './ctaCard.vue';
export default {
    name: 'CallToAction',
    components:{
        ctaCard,
    }
}
</script>

<template>
    <div class="row">
        <div class="col-6 left ">
            <h2>Let's Make Things Happen</h2>
            <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste animi corrupti sapiente mollitia saepe nulla necessitatibus magnam rem</h3>
            <i>"The tema at Avada Marketing Consultant is Fabulous. They helped us unlock our potential online and offline. We have experienced year on year growth dur to their progressive approach"
            </i>
            <div class="ref">
                <h6>George Anderson</h6>
                <p>DigitalBox CEO</p>
            </div>
        </div>
        <div class="col-6 right">
            <ctaCard/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
.right{
    padding-left: 75px;
    .sc-card{
        box-shadow:none;
    }
}

.left{
    h2{
        font-size: 70px;
        
    }
    h3{
        font-size: 1.9rem;
        &:after{
            content: '';
            display: block;
            width: 15%;
            border-bottom: 1px solid white;
            margin-top: 30px;
        }
    }
    i{
        font-size: 1.4rem;
    }

    h6{
        font-size: 20px;
    }
    p{
        color: gray;
    }
    & > *{
        margin-bottom: 30px;
    }
}
</style>