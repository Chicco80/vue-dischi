<template>
    <section class="container">
        <AppSearch @performSearch="mySearch" :listGenre="genre"/>
        <div class="row">
            <div v-for="album in filteredmusicList" :key="album.index" class="col">
                <app-card :item="album"/>
            </div>
        </div> 
    </section>
</template>

<script>
import axios from 'axios'
//import AppLoader from './AppLoader.vue'
import AppCard from './AppCard.vue'
import AppSearch from './AppSearch.vue'
export default {
    name: 'AppGrid',
    components: {
    //AppLoader,
    AppCard,
    AppSearch,
    
    },
    data(){
        return{
            apiPath:'https://flynn.boolean.careers/exercises/api/array/',
            musicList:[],
            genre:[],
            searchText:'',
            
            //loading:false,
        }
        
    },
    methods:{
        mySearch(text){
            this.searchText = text;
        }
    },
    computed:{
        filteredmusicList(){
            if(this.searchText === ""){
                return this.musicList;
            }
            return this.musicList.filter((item)=>{
                return item.genre === this.searchText
                
            });
        }
    },
    mounted(){
        // this.loading=true;
        axios.get(this.apiPath + 'music').then((res)=>{
            // console.log(res);
            this.musicList = res.data.response
            this.musicList.forEach((el)=>{
                if(!this.genre.includes(el.genre)){
                    this.genre.push(el.genre);
                }
            });
            //console.log(res.data.response)
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