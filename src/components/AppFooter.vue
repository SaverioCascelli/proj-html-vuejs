<script>
import { store } from '../data/store';
import socials from '../data/socials'
import footerMenu from '../data/footerMenu';
export default {
    name:'AppFooter',
    data(){
        return{
            store,
            socials,
            footerMenu,
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="row top">
                <div class="col-4">
                    <h3>Grow Your Online Business Strategically, and Improve Custormer Retention.</h3>
                    <div class="socials d-flex">
                        <a 
                        v-for="(element, key) in socials"
                        :key="key"
                        href="#"><i :class="element.icon"></i></a>
                    </div>
                </div>
                <div class="col d-flex justify-content-start right">
                    <ul v-for="(element,key) in footerMenu" :key="key">
                        <h6>{{element.title}}</h6>
                        <li v-for="(ele,i) in element.linkList" :key="i">
                        <a :href="ele.src">{{ele.txt}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="row bottom justify-content-between">
                <div class="col-auto">
                    <p><i class="fa-regular fa-copyright"></i>Avada Consultant Powered by Boolean</p>
                </div>
                <div class="col-5">
                    <p>Call Us {{store.phoneNumber}} </p>
                </div>
                <div class="col-auto">
                    <p>{{store.mail}}</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *; 
.top{
    padding-top: 120px;
    .right{
        h6,li{
            margin-bottom: 20px;
        }
        ul{
            list-style: none;
            width:250px;
        }
        a{
            text-decoration: none;
            color: black;
        }
    }
}

.bottom{
    font-size: 1rem;
    margin: 100px 0;
    i{
        font-size: .8rem;
    }
}
.socials > *{
    color: black;
    margin-left: 20px;
    font-size: 1.3rem;
}

</style>