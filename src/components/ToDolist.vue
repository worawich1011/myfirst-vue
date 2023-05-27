<template>
        <ul>   
            <ListData 
                v-for="(item,index) in todos" 
                :key="index"
                :list="item.list"
                :id="index"
            />
        </ul>
</template>

<script>

import ListData from './ListData.vue';
export default {
    name:"ToDolist",
    components:{
        ListData
    },
    props:["todos"],
    methods:{
    
    }
}
</script>

<style scoped>
    h1{
        color: aliceblue;
    }
    ul{
        list-style: none;
    }

</style>