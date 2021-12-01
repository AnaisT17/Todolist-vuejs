<template>
<div>
    <div class="header-top">
        {{ titre }}

    </div>
</div>
</template>
<script>

export default{
    name:'Header',
    data(){
    return{
        titre: 'To do List !'
    }
    }
}
</script>
<style scoped>

.header-top{
    position: fixed;
    top:0;
    height: 50px;
    background: gray;
    color: azure;
    width: 100%;
    text-align: center;
    line-height: 50px;
    font-size:25px;
}


</style>