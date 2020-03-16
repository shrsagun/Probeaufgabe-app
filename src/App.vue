<template>
    <div id="app">
        <Header/>
        <router-view/>
    </div>
</template>

<script>

import Header from '@/partials/Header';
export default {
    name: 'App',
    components: {
        Header
    }
}
</script>

<style>
body,td,th {
    font-family: Arial, sans-serif;
    font-size: 16px;
    margin: 0px;
    padding: 0px;
}
</style>
