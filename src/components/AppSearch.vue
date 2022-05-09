<template>
<div>
    <select name="genre" id="genre" class="my-5" v-model="inputText" @change="search">
        <option value="">All</option>
        <option value="genere" v-for="genere in listGenre" :key="genere.index">{{genere}}</option>
        
    </select>
</div>
    
</template>

<script>
export default {
    name:'AppSearch',
    data(){
        return{
            inputText:'',
        }
    },
    props:['listGenre'],
    methods:{
        search(){
            this.$emit("okSearch", this.inputText);
            this.inputText ="";
            
        }
    }
}
</script>

<style lang="scss" scoped>

</style>