<template>
    <div class="card p-4 mb-3" style="width: 14rem;">
        <img :src="item.poster" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{item.title}}</h5>
            <div class="card-text">{{item.author}}</div>
            <div class="card-text">{{item.year}}</div>
        </div>
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
@import "@/assets/styles/general.scss";
.card{
    width: 18rem;
    height: 350px;
    background-color: $nav-color;
}
.card-img-top{
    width: 100%;
    height: 100%;
}
h5{
    text-align: center;
    color: $title-clr;
}
.card-text{
    text-align: center;
    color: $text-clr;
}

</style>