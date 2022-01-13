<template>
    <header>
        <h1>{{title}}</h1>
        <Button @show-add-task="$emit('toggle-add-task')" :text="showaddtask ? 'Close' : 'AddTask'" :color="showaddtask ? 'red' : 'green'"/>
    </header>
</template>


<script>
import Button from './Button'
export default {
    name:'Header',
    props:{
        title:{
            type:String,
            default:"Tareq",
            
        },
        showaddtask:Boolean,
    },
        components:{
            Button,
        },
        
        
    

}
</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>