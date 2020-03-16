<template>
    <div id="header">
        <h1>Bitcoin </h1>
        <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/bitcoin-details">Bitcoin Details</router-link> |
            <router-link to="/about">About</router-link> |
            
        </div>
    </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    #header {
        background-color: #555555;
        padding: 1em;
        border-bottom: solid 1px #444444;
        box-shadow: 0px 0px 7px #CCC;
	}
    
    #header h1 {
        color: #FFF;
    }
    #header a {
        text-decoration: none;
        color: #EAEAEA;
    }
    #nav {
        color: #FFF;
    }
</style>

