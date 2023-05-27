<template>
    <div class="css">
        <h1>My Todolist</h1>
        <hr>
        <form >
            <div class="form-control">
                <label for="">Add your new todo : &nbsp; </label>
                <input type="text" v-model="todo.list">
                <button @click.prevent="submitform">Add</button>
            </div>
        </form>   
    </div>

</template>

<script>

export default {
    name:"FormTdo",
    data(){
        return{
            todo:{
                list:"",
                id:0,
            }
        }
    },
    components:{
    },
    methods:{
        submitform(){
            const newList={
                list:this.todo.list,
            }
            this.$emit("save", newList);
            this.resetForm();          
        },
        resetForm(){
            this.todo.list="";
        }
    },
}
</script>

<style scoped>
    .css{
        background: #fff;
        text-align: center;
        border-radius: 15px 15px 0px 0px;
        padding: 1rem;
        margin: 3rem;
        width: 60%;
        margin-top: 10%;
        margin-left: 20%;
        margin-bottom: 0%;
    }
    button{
        background: rgb(77, 77, 255);
        color: #fff;
        width: 80px;
        
    }
    button:hover{
        transition: 0.25s;
        background: #fff;
        color: rgb(77, 77, 255);
        width: 80px;
    }
    
</style>