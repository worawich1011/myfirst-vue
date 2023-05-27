<template>
    <li>
        <h3>{{ list }}</h3>
    </li>
        
</template>

<script>



export default {
    name:"ListData",
    components:{

    },
    props: {
        list:{
            type:String,
            requierd:true
        },
        id:{
            type:Number,
            required:true
        },
    }
    ,
    methods:{

    }
}
</script>

<style scoped>
    img{
        position:absolute;
        left: 65%;
        width: 30px;
        cursor: pointer;
    }
    li{
        list-style: none;
        background: #fff;
        text-align: start;
        padding: 1rem;
        width: 60%;
        margin-left: 17.94%;
        width: 61.6%;
        display:flex;
        
    }
    li:hover{
        transition: 0.6s;
        opacity: 50%; 
    }
</style>