<template>
    <div class="row">
        <the-quote v-for="quote in quotes" :key="quote.message"> 
            {{quote.message}}
        </the-quote>
    </div>
</template>

<script>
import TheQuote from './TheQuote.vue'

export default {
    props:['quotes'],
    components:{
        TheQuote
    },
    
}
</script>

<style>
    
</style>