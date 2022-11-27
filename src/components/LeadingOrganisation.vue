<script>
import organisationCards from '../data/organisationCards';
import leadingOrganisationCard from './leadingOrganisationCard.vue';
export default {
    name:'LeadingOrganisation',
    components:{
        leadingOrganisationCard,
    },
    data(){
        return{
            organisationCards,
        }
    }
}
</script>

<template>
    <div class="row text-center">
        <div class="col">
            <h2>Trusted by Leading organisation</h2>
            <div class="card-wrapper d-flex justify-items-between gap-5">
                <leadingOrganisationCard
                v-for="(element, key) in organisationCards "
                :key="key"
                :cardData="element"
                />
            </div>
            <a href="#" class="col-auto mx-auto sc-button full">Read More Case Studies</a>
        </div>
    </div>
    
</template>

<style lang="scss" scoped>
@use '../style/partials/sc-button.scss' as *;
@use '../style/general.scss' as *;

h2{
    margin-bottom: 90px;
}
.card-wrapper{
    margin-bottom: 75px;
}

</style>