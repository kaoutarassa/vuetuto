<template>
    
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    el: "#app",
    data: {
        simpleMenu: [
            {
            name: "Croissant",
            image: {
                source: "/image/croissant.jpg",
                alt: "Un croissant"
            },
            inStock: true,
            quantity: 1
            },
            {
            name: "Baguette de pain",
            image: {
                source: "/image/french-baguette.jpeg",
                alt: "Quatre baguettes de pain"
            },
            inStock: true,
            quantity: 1
            },
            {
            name: "Éclair",
            image: {
                source: "/image/eclair.jpg",
                alt: "Éclair au chocolat"
            },
            inStock: false,
            quantity: 0
            }
            ],
}})
</script>
<style lang="scss">

</style>