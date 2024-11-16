<template>
    <div>
        <div class="wrapper">
            <h1>d Component</h1>
            <h2>{{ count }}</h2>
            <button @click="sendDate">send count</button>
        </div>
    </div>
</template>

<script setup>

import {inject, defineEmits, ref} from "vue";

const count=ref(0);
const user=inject("user");

const emit=defineEmits();

const users=[
    {
        id:1,
        name:"khusi",
        age:20,
        profession:"IT"
    },
    {
        id:1,
        name:"khusi",
        age:20,
        profession:"IT"
    },
    {
        id:1,
        name:"khusi",
        age:20,
        profession:"IT"
    },
    {
        id:1,
        name:"khusi",
        age:20,
        profession:"IT"
    },
]

const sendDate=()=>{
    emit("counter", 11);
    emit("users", users);
}

</script>

<style scoped>
.wrapper{
    background-color: rgba(191, 255, 0, 0.393);
    padding: 50px;
    border: 2px solid red;
}
</style>