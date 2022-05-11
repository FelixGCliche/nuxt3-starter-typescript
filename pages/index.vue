<template>
  <div class="grid">
    <div class="cell cell-full">
      <h1 class="display">Lorem Ipsum</h1>
    </div>
    <div class="cell">
      <p class="body">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat
        condimentum congue nulla nulla netus amet pulvinar faucibus.
      </p>
      <ButtonPrimary url="/contact" label="Local link" />
    </div>
    <div class="cell">
      <p class="body">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat
        condimentum congue nulla nulla netus amet pulvinar faucibus.
      </p>
      <a href="https://github.com/FelixGCliche/nuxt3-starter-typescript">
        <ButtonPrimary label="External link" />
      </a>
    </div>
    <div class="cell">
      <p class="body">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat
        condimentum congue nulla nulla netus amet pulvinar faucibus.
      </p>
      <ButtonPrimary label="Custom button click" @button-click="handleClick" />
    </div>
  </div>
</template>

<script lang="ts" setup>
const handleClick = (e: Event) => {
  console.log(`Button click handled with raised event ${e}`)
}
</script>

<style lang="scss" scoped>
@use 'sass:map';

.grid {
  @include layout.layout-grid;
}
.cell {
  @include layout.responsive-cell {
    &-full {
      @include layout.grid-cell-full;
    }
  }
}
</style>
