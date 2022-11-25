<script>
export default {
    name:'ctaCard',

}
</script>

<template>
    <div class="sc-card">
        <div class="current-marketer text-center">
            <div class="sc-card-img m-auto">
                <img src="../assets/marketing-consultant-expert.jpg" alt="">
            </div>
            <h5>Richard Madsen</h5>
            <p>Marketing Consultant Expert</p>
            <p class="col-ecstasy"><i class="fa-solid fa-phone"></i> ( 555) 802-0124</p>
        </div>
        
        <div class="bottom-form">
        <form action="">
            <input type="text" class="form-control" placeholder="Your Name*">
            <input type="email" class="form-control" placeholder="Your Email*">
            <input type="number" class="form-control" placeholder="Your Phone Number*">
        </form>
        <button class="sc-button">Get a Callback</button>
        <p class="little-text text-secondary">By submitting my data i agree to be contacted</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;
@use '../style/partials/sc-button.scss' as *;
@use '../style/partials/variables' as *;
    .sc-card{
        width: 475px;
        background: white;
        height: 360ps;
        border-radius: 15px;
        box-shadow: 2px 2px 5px lightgray;
        display: flex;
        flex-direction: column;
        align-items:stretch;
        padding: 2rem;
        .sc-card-img{
            width: 80px;
            border-radius: 50%;
            overflow: hidden;
        }
        .bottom-form{
            margin-top: 20px;
            input{
                height: 3.5rem;
                margin: 15px 0;
            }
            .sc-button{
                width: 100%;
                background: $ecstasy;
                color: white;
            }
            .little-text{
                text-align: center;
                font-size: .8rem;
                padding-top: .5rem;
            }
        }
    }
</style>