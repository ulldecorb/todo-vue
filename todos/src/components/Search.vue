<template>
    <div>
        <div id="search-container">
            <input type="text" v-model="query" v-on:input="$emit('query-change' ,query)">
        </div>
    </div>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default {
    name: 'Search',
    data(){
        return {
            query: ''
        }
    }
}
</script>

<style scoped>
    #search-container {
        width: 600px;
        margin: 0 auto;
    }

    input {
        padding: 10px;
        width: 100%;
        outline: none;
    }
</style>