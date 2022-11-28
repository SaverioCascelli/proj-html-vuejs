<script>

export default {
    name:'fixedMsg'
}
</script>
<template>
    <div class="smg-box">
        we
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss' as *;

.smg-box{
    position: fixed;
    right: 50px;
    bottom: 50px;
    z-index: 999;
}

</style>