<script>
export default {
    name:'Testimonials',
}
</script>

<template>
    <div class="row testimon">
        <div class="col-6">
            <div class="img-wrapper">
                <img src="../assets/large-testimonial-600x583.jpg" alt="">
            </div>
        </div>
        <div class="col-6">
            <div class="text-wrapper">
                <h3>"The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online and offline. We have experienced year on year growth due to their progressive aaproach."</h3>
                <h6>Kate Schadler</h6>
                <p>Marketing Consultant-Abstract</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.testimon{
    margin: 100px 0;
}
.img-wrapper {
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 3px 3px 3px gray;
}

.text-wrapper{
    padding: 75px;
    padding-right: 30%;
    h3{
        margin-bottom:40px ;
    }
    p{
        font-size: .8rem;
    }
}

</style>