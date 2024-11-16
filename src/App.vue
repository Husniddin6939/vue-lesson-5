<template>

    <header>
        <nav>
            <ul>
                <li><router-link to="/">home</router-link></li>
                <li><router-link to="/about">about</router-link></li>
                <li><router-link to="/contact">contact</router-link></li>
                <li><router-link to="/service">service</router-link></li>
            </ul>
        </nav>
    </header>

    <main>
       <router-view></router-View>
    </main>

    <footer>
        <p>footer</p>
    </footer>
</template>

<script setup>

</script>

<style scoped>
main{
    min-height: 100vh;
}

</style>