<template>
    <div class="book-list">
        <BookCard v-for="book in $books" :key="book.id"  />
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'
    import { books } from '@/store'

    export default Vue.extend({
        computed: {
            $books() {
                return books.$all
            }
        }
    })
</script>

<style lang="scss" scoped>

</style>