<script>

export default {
    name:'fixedMsg'
}
</script>
<template>
    <div class="wrapper d-flex flex-column align-items-end">

        
        <div class="box-cha mb-3 pt-4 px-2">
            <div class="img-wrapper">
                <img src="../assets/marketing-expert-cta.png" alt="">
            </div>
            <p>This is a free HubSpot live chat. You can create your own chat flows and engage your customers with Avada & HubSpot!</p>
            <div class="close"><i class="fa-solid fa-xmark"></i></div>
        </div>
        <div class="smg-box">
            <i class="fa-solid fa-comments"></i>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/variables' as *;

.smg-box{
    background: $primary;
    width: 65px;
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
    color: white;
}

.box-cha{
    width: 250px;
    background: white;
    box-shadow: 1px 1px 5px 1px lightgray;
    position:relative;
    .close{
        position: absolute;
        right: 10px;
        top: 5px;
    }
}

.wrapper {
    position: relative;
    .img-wrapper{
        position: absolute;
        width: 60px;
        transform: translate(-50%, -50%);
        left: 50%;
        top: -10px;
        border-radius: 50%;
        aspect-ratio:  1 / 1;
        overflow: hidden;
    }
}

</style>