<script>
import awardsCard from './awardsCard.vue';
import geConsulationCard from './geConsulationCard.vue';
import dataAwards from '../data/awards'
export default {
    name:'feature',
    components:{
        awardsCard,
        geConsulationCard,
    },
    data(){
        return{
            cardObj:{
                imgName: 'we-boost-our-clients-600x549.jpg',
                title: "We Boost Our Client'Bottom Line by Optimizing Their Growth Potential.",
                text: 'Quisque aliquet, libero ocnsequat elementum convallis, erata risus imperdiet pellentesque sem neque erget.',
                buttonText: 'Why Work With Us'
            },
            dataAwards

        }
    }
}
</script>

<template>
    <geConsulationCard
    class="feature-card"
    :cardData="cardObj"
    />

    <div class="row">
        <div class="col-6 left">
            <h3>We Build Relationships</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat rerum similique et accusamus unde quod veritatis debitis. Numquam, beatae neque!</p>
            <h3>Proprietary Processes</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat rerum similique et accusamus unde quod veritatis debitis. Numquam, beatae neque!</p>
        </div>
        <div class="col-6 d-flex flex-column right">
            <div class="feature-box d-flex">
                <div class="box">
                    <i class="fa-brands fa-searchengin"></i>
                </div>
                <div class="text">
                    <h4>Accountability</h4>
                    <p>Lorem ipsum dolor sit amet.</p>
                </div>
            </div>
            <div class="feature-box d-flex">
                <div class="box">
                    <i class="fa-brands fa-searchengin"></i>
                </div>
                <div class="text">
                    <h4>Transparency</h4>
                    <p>Lorem ipsum dolor sit amet.</p>
                </div>
            </div>
            <div class="feature-box d-flex">
                <div class="box">
                    <i class="fa-brands fa-searchengin"></i>
                </div>
                <div class="text">
                    <h4>Investment</h4>
                    <p>Lorem ipsum dolor sit amet.</p>
                </div>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col text-center">
            <h3>Awards</h3>
             <div class="container-fluid">
                <div class="row justify-content-between">
                    <awardsCard
                    v-for="(element, key) in dataAwards"
                    :key="key"
                    :dataAward="element"
                    />
                </div>
             </div>
        </div>
    </div>
</template>
 
<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;

.left p{
    margin-bottom: 75px;
    font-size: 1.2rem;
}
.right{
    padding-left: 110px;
}
.feature-card{
    flex-direction: row-reverse;
}

.feature-box{
    margin-bottom: 60px;
    .box{
        margin: 0 20px;
        display: flex;
        width:75px ;
        aspect-ratio: 1 / 1;
        border: 2px solid $primary;
        color: $primary;
        border-radius: 15px;
        i{
            font-size: 40px;
            line-height: 75px;
            text-align: center;
            width: 100%;
        }
    }
}
</style>