<template>
    <div>
        <div class="wrapper">
            <h1>a Component</h1>
            <ComponentB @counter="submitEmit" @users="submitUser"/>
        </div>
    </div>
</template>

<script setup>
import ComponentB from "./b-component.vue";
import {defineEmits} from "vue";

const emit=defineEmits();

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
    background-color: rgba(0, 255, 0, 0.393);
    padding: 50px;
    border: 2px solid red;
}
</style>