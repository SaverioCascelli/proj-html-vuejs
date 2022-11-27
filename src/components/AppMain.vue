<script>
import './geConsulationCard.vue'
import GeConsulationCard from './geConsulationCard.vue';
import Affiliate from './Affiliate.vue';
import ConsulationCard from '../data/ConsulationCard'
import LeadingOrganisation from './LeadingOrganisation.vue';
export default {
    name: "appMain",
    components: {
        GeConsulationCard,
        Affiliate,
        LeadingOrganisation,
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
    </main>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
.get-consultation{
    margin-top:150px;
    & >:nth-of-type(even){
        flex-direction: row-reverse;
    }
}

.leading-org{
    margin-bottom: 130px;
}


</style>
