<script>
import './geConsulationCard.vue'
import GeConsulationCard from './geConsulationCard.vue';
import Affiliate from './Affiliate.vue';
export default {
    name: "appMain",
    components: {
        GeConsulationCard,
        Affiliate,
     }
}
</script>

<template>
  
    <main>
        <section class="get-consultation container">
        
            <GeConsulationCard/>
            <GeConsulationCard/>
            <GeConsulationCard/>
            
        </section>
        <section class="container affiliate-comp">
            <Affiliate/>
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


</style>
