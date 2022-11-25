<script>
import './geConsulationCard.vue'
import GeConsulationCard from './geConsulationCard.vue';
export default {
    name: "appMain",
    components: "geConsultationCard",
    components: { GeConsulationCard }
}
</script>

<template>
  
    <main>
        <section class="get-consultation container">
        
            <GeConsulationCard/>
            <GeConsulationCard/>
            <GeConsulationCard/>
            
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
