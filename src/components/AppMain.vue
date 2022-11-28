<script>
import Advice from './Advice.vue';
import Testimonials from './Testimonials.vue';
import './geConsulationCard.vue'
import GeConsulationCard from './geConsulationCard.vue';
import Affiliate from './Affiliate.vue';
import ConsulationCard from '../data/ConsulationCard'
import LeadingOrganisation from './LeadingOrganisation.vue';
import Feature from './feature.vue';
export default {
    name: "appMain",
    components: {
        Advice,
        GeConsulationCard,
        Affiliate,
        LeadingOrganisation,
        Feature,
        Testimonials,
     },
     data(){
        return{
            ConsulationCard,
        }
     }
}
</script>

<template>
  
    <main>
        <section class="get-consultation container">
        
            <GeConsulationCard
            v-for="(element,index) in ConsulationCard"
            :key="index"
            :cardData="element"
            />
            
        </section>
        <section class="container affiliate-comp">
            <Affiliate/>
        </section>
        <section class="container leading-org">
            <LeadingOrganisation/>
        </section>
        
        <div class="feature-wrapper">
            <section class="container feature">
                <feature/>
            </section>
        </div>

        <section class=" container testimonials">
            <Testimonials/>
        </section>

        <section class="advice ">
            <div class="container">
                
                <Advice/>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;
.get-consultation{
    margin-top:150px;
    & >:nth-of-type(even){
        flex-direction: row-reverse;
    }
}

.leading-org{
    margin-bottom: 130px;
}  

.feature-wrapper{
    background: $grayNurse;
    padding-top: 80px;
    padding-bottom: 120px ;
}

.testimonials{
    margin-top:100px;

}
.advice{
    padding: 150px 0;
    background: $grayNurse;
}

</style>
