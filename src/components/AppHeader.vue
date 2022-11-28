
<script>
import headerNav from '../data/headerNav';
export default {
    name:'AppHeader',
    data(){
        return{
            headerNav,
        }

    }
}
</script>

<template>
    
    <header class="d-flex align-items-center justify-content-between">
        <div class="logo col-2">
            <img src="/avada-marketing-logo.png" alt="">
        </div>

        <nav class="col">
            <ul class="sc-list">
                <li
                v-for="(element,key) in headerNav" :key="key"
                ><a :class="{'active':element.active}" href="#">
                {{element.mainTxt}}
                <i v-if="element.childTxt" class="fa-solid fa-chevron-down"></i>
                </a></li>
                <!-- <li><a class="sc-dropdown active" href="#">Home <i class="fa-solid fa-chevron-down"></i></a></li>
                <li><a class="sc-dropdown" href="#">Services <i class="fa-solid fa-chevron-down"></i></a> </li>
                <li><a href="#">Why Us</a> </li>
                <li><a href="#">Case Studies</a> </li>
                <li><a href="#">About</a> </li>
                <li><a href="#">Blog</a> </li> -->
            </ul>
        </nav>
        
        <div class=" quote col-4 d-flex justify-content-between align-items-center h-100 ">
            <div class="px-5"><i class="fa-solid fa-phone"></i> <span>(555) 802-1234</span></div>
            <div>
                <button type="button" class="sc-button btn">Free Quote</button>
            </div>
        </div>
</header>

</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/sc-button.scss' as *;

header{
    height: 115px;  
    font-weight: 600;

    nav{
        height: 100%;
        padding: 0 20px;
    }

    .sc-list{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        list-style-type: none;
        padding-right: 0px;
        li{
            padding: 0 7px;
        }
        a{
            padding-left: 5px;
            text-decoration:none;
            color: black;
            line-height: 35px;
            &.active{
                color: $ecstasy;
            }
            &.active:after{
                border-color: $ecstasy;
            }
            &:hover{
                color: $ecstasy;
            }
            &:hover:after{
                border-color: $ecstasy;
            }
            &:after{
                content: "";
                display: block;
                width: 100%;
                border-bottom: 3px solid rgba($ecstasy, $alpha: 0);
            }
            font-size: 1.1rem;
            i{
                font-size: .8rem;
            }
        }
    }

    .quote{
        i{
            color: $ecstasy;
        }
    }


}
</style>