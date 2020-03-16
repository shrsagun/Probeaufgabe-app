<template>
    <div class="dashboard">
        <h3>Current exchange rates for bitcoin</h3>
        <div v-for="(rate, key) in rates" v-bind:key="rate">
            <ul class="exchnge-rates">
                <li>{{key}}:</li>
                <li>Buying Price: {{ rate.buy }} {{ rate.symbol }}</li>
                <li>Selling Price: {{ rate.sell }} {{ rate.symbol }} </li>
            </ul>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    props: ['rates'],
    created() {
        axios.get("https://blockchain.info/ticker")
            .then(res => this.rates = res.data)
            .catch(err => console.log(err))
    }
}
</script>

<style scoped>
    .exchnge-rates {
        list-style-type: none;
    }
    .exchnge-rates li {
        display: inline-block;
        padding-right: 1rem;
    }
</style>