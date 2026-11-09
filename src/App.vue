<script setup lang="ts">
import { onMounted } from 'vue'
import { storeToRefs } from 'pinia'
import { RouterLink, RouterView } from 'vue-router'
import { useDeliveryStore } from './store'
const store = useDeliveryStore()
const { approvedShare, offers, urgent } = storeToRefs(store)
onMounted(store.load)
</script>

<template><div class="shell"><aside><div class="brand">ProductDataEU<span>ACCESS REQUESTS</span></div><nav><RouterLink to="/">Data requests</RouterLink><RouterLink to="/insights">Access guidance</RouterLink></nav><div class="health"><i /> Java data service connected</div></aside><main><header><div><span class="eyebrow">Give connected-product users practical control over the data they generate</span><h1>Connected Product Data Access Desk</h1></div><button @click="store.addOffer">Add data request</button></header><section class="summary"><article><small>Requests approved</small><strong>{{ approvedShare }}%</strong><div class="bar"><span :style="{ width: `${approvedShare}%` }" /></div></article><article><small>Requests tracked</small><strong>{{ offers.length }}</strong><p>Shared access view</p></article><article><small>Urgent access gaps</small><strong>{{ urgent }}</strong><p>Needs attention</p></article></section><RouterView /></main></div></template>
