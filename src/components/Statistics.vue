<template>
    <div class="statistics">
        <h3>Statistics</h3>
        <ul>
            <li>Market cap: </li>
            <li>Number of bitcoins in circulation: {{ stats.totalbc }}</li>
            <li>Number of transactions in the last 24 hours: {{ stats.n_tx }}</li>
            <li>Number of bitcoins sent in the last 24 hours:{{ stats.total_btc_sent }}</li>
            <li>Current hash rate: {{ stats.hash_rate }}</li>
            <li>Current level of difficulty: {{ stats.difficulty }}</li>
        </ul>
    </div>
</template>

<script>

import statistics from 'blockchain.info/statistics';

export default {

    name: 'Statistics',
    props: [
        'stats'
    ],

    created() {
        statistics.get({timestamp: '1d'})
        .then(res => this.stats = res)
        .catch(err => console.log(err))
    }
}
</script>

<style scoped>

</style>
