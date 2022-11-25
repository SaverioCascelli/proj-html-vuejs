<script>
export default {
    name:'getConsulationCard',
}
</script>

<template>
   
    <div class="row ">
        <div class="col-6">
            <div class="img-wrapper">
                <img src="../assets/adventure_thumbnail-400x300.jpg" alt="">
            </div>
        </div>
            <div class="text col-6">
                <div class="top-feature">
                    <div class="svg">svg</div>
                    <span>Business Growth</span>
                </div>
                <h2>Increase Brand Awareness</h2>
                <div class="info-text">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At fuga sequi ipsum impedit nisi dolor itaque enim veniam provident aliquid fugiat consequuntur quisquam ipsam dolorem nihil, harum ducimus exercitationem explicabo.</p>
                </div>
                <a href="#" class="sc-button full">Get Consultation</a>
                
            </div>
        <div class="col-6"></div>
    </div>

</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/sc-button.scss' as *;
@use '../style/partials/variables' as *;

.row > *{
    padding: 0 50px;
     margin: 50px auto;
}
    .img-wrapper{
        width: 500px;
    }
    .text{
        text-align: left;
        .svg{
            width: 40px;
            display: inline-block;
            margin-right: 10px;
            aspect-ratio: 1 / 1;
            border-radius: 50%; 
            color: white;
            line-height: 40px;
            background: $ceruleanBlue;
            text-align: center;
        }

        .info-text{
            max-height: 140px;
            overflow: auto;
            margin-bottom: 30px;
        }

        h2{
            font-size: 3rem;
        }
        p{
            font-size: 1.5rem;
            
        }
    }


</style>