<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
    name: 'App',
    components:{
        AppHeader,
        AppMain,
        AppFooter,
    },  
}


</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <AppHeader/>

                <AppMain/>
                <AppFooter/>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use './style/general.scss' as  *;

</style>