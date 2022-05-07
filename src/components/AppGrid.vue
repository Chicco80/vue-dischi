<template>
    <section class="container">
        
        <!-- <AppLoader/> -->
        <!-- <div v-for="item in musicList" :key="item.index">
            autore {{item.author}} - {{item.genre}} - {{item.title}} - {{item.year}}
            <img :src="item.poster" alt="">
        </div>  -->
        <div class="row">
            <div v-for="album in musicList" :key="album.index" class="col">
                <app-card :item="album"/>
            </div>
        </div>
    </section>
</template>

<script>
import axios from 'axios'
// import AppLoader from './AppLoader.vue'
import AppCard from './AppCard.vue'
export default {
    name: 'AppGrid',
    components: {
    //     AppLoader
    AppCard
    },
    data(){
        return{
            musicList:[],
            apiPath:'https://flynn.boolean.careers/exercises/api/array/',
            loading:false,
        }
    },
    mounted(){
        // this.loading=true;
        axios.get(this.apiPath + 'music').then((res)=>{
            // console.log(res);
            this.musicList = res.data.response
            console.log(res.data.response)
            // this.loading=false;
        }).catch((error)=>{
            console.log(error)
            // this.loading=false;
        })
        
    },
}
</script>

<style lang="scss" scoped>

</style>