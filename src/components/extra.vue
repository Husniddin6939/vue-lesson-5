<template>
    <h1>Parent Component</h1>
<div class="wrapper">
    <h1>{{ user }}</h1>
    <!-- <input type="text" placeholder="Enter username" v-model="user.name"> -->
    <ComponentA :user="user" @counter="submitEmit" @users="submitUser" />
</div>
</template>

<script setup>
import ComponentA from "./components/a-component.vue";
import {reactive, provide} from "vue";


const user=reactive({
name:"Jahongir",
age:30,
})

provide("user", user)


const submitEmit=(e)=>{
console.log(e);
}

const submitUser=(e)=>{
console.log(e);
}



</script>

<style scoped>
.wrapper{
background-color: #f0f0f0;
padding: 120px;
}
</style>