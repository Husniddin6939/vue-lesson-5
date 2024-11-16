<template>
    <div>
        <div class="wrapper">
            <h1>b Component</h1>
           
            <ComponentC @counter="submitEmit" @users="submitUser"/>
        </div>
    </div>
</template>

<script setup>
import {defineEmits} from "vue";
import ComponentC from "./c-component.vue";

const emit=defineEmits()


const submitEmit=(e)=>{
    console.log(e)
    emit("counter", e);
    
}

const submitUser=(e)=>{
    console.log(e)
    emit("users", e);
}

</script>

<style scoped>
.wrapper{
    background-color: rgba(38, 0, 255, 0.393);
    padding: 50px;
    border: 2px solid red;
}
</style>