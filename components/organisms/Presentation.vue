<template>
    <div class="presentation">
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis labore voluptates rerum reprehenderit dolorum sequi aliquid voluptatum saepe excepturi vel modi mollitia neque accusantium aperiam laborum velit sunt, repellat illo?
        </p>

        <img src="@/assets/img/presentation.svg" alt="Presentation of iBook">
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        
    
    })
</script>

<style lang="scss" scoped>

.presentation {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 2rem;
  align-items: center;
  @include screen('small', 'medium') {
    grid-template-columns: 1fr;
  }
  p {
    line-height: 26px;
  }
  img {
    max-width: 100%;
  }
}

</style>