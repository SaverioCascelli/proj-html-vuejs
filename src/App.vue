<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';
export default {
    name: 'App',
    components:{
        AppHeader,
        AppMain,
        AppFooter,
        AppJumbotron,
    },  
}


</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <AppHeader/>
            </div>
        </div>
    </div>
    <div class="container-fluid">
        <div class="row">
            <div class="col"></div>
            <AppJumbotron/>
        </div>
    </div>
                <AppMain/>
                <AppFooter/>
</template>

<style lang="scss">
@use './style/general.scss' as  *;

</style>