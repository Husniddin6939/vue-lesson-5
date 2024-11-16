<template>
    <div>
        <div class="wrapper">
            <h1>c Component</h1>
        
            <ComponentD @counter="submitEmit" @users="submitUser"/>
        </div>
    </div>
</template>

<script setup>
import {defineEmits} from "vue";
import ComponentD from "./d-component.vue";

const emit=defineEmits();

const submitEmit=(e)=>{
    console.log(e);
    emit("counter", e)
    
}

const submitUser=(e)=>{
    console.log(e);
    emit("users", e);
}

</script>

<style scoped>
.wrapper{
    background-color: rgba(255, 0, 217, 0.393);
    padding: 50px;
    border: 2px solid red;
}
</style>