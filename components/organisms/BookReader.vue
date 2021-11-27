<template>
    <div class="book-reader">
        <h2 class="book-title">{{ $book.title }}</h2>

        <div class="gallery-container">

            <div class="swiper-container">

                <div class="swiper-wrapper">

                    <div 
                    v-for="page in $book.pages"
                    :key="page.id"
                    class="swiper-slide gallery-pages"
                    >
                    <img src="@/assets/img/page.svg" :alt="`Pagina ${page.pageNumber} do livro ${$book.title}`">
                    <p>{{ page.pageNumber }}</p>
                    </div>

                </div>

            </div>

            <div class="swiper-container gallery-main">

                <div 
                v-for="page in $book.pages" 
                :key="page.id"
                class="swiper-slide page">
                    <p v-html="page.text"></p>
                </div>

            </div>


            <div class="buttons-container">

                <div class="prev">
                    <img src="@/assets/img/arrow.svg" alt="Ler pagina anterior">
                </div>

                <div id="right-arrow" class="next">
                    <img src="@/assets/img/arrow.svg" alt="Ler próxima pagina">
                </div>

            </div>

        </div>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'
    import { books } from '@/store'

    export default Vue.extend({
        computed: {
            $book() {
                return books.$single
            }
        }
    })
</script>

<style scoped>

</style>