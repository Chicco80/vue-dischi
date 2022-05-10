<template>
<div>
    <select name="genre" id="genre" class="my-5" v-model="inputText" @change="goSearch">
        <option value="">All</option>
        <option :value="genere" v-for="(genere, index) in listGenre" :key="index">{{genere}}</option>
        
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
        goSearch(){
            this.$emit("performSearch", this.inputText);
            console.log(this.inputText)
            this.inputText ="";
            
            
        }
    }
}
</script>

<style lang="scss" scoped>

</style>