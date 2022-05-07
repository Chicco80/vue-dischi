<template>
    <div class="card "> 
        <img :src="item.poster" class="card-img" alt="">
        <h4>{{item.title}}</h4>
        <div>{{item.author}}</div>
        <div>{{item.year}}</div>
    </div>
</template>

<script>
export default {
    name:'AppCard',
    props:{
        item: Object
    }
}
</script>

<style lang="scss" scoped>
.card{
    width: 18rem;
    height: 350px;
}

</style>