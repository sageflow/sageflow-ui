<template lang="pug">
ul.options-switch
    li.option(
      v-for="(option, idx) in options",
      :class="{ 'selected': idx == selectedIndex }"
      @click="() => selectClicked(idx)"
    ) {{option}}
</template>

<script>
  import { ref } from "vue"

  export default {
    props: {
      options: Array,
    },
    setup() {
      let selectedIndex = ref(0)

      const selectClicked = (idx) => {
        selectedIndex.value = idx
      }

      return {
        selectedIndex,
        selectClicked,
      }
    },
  }
</script>

<style lang="scss" scoped>
  ul.options-switch {
    height: 1.8rem;
    min-height: 1.8rem; // Needed to maintain height on Firefox at different scales.
    background-color: var(--color-bg-6);
    display: flex;
    align-items: center;
    font-size: 0.9rem;
    border-radius: var(--border-rad-xl);
    padding: 0.125rem;
    cursor: pointer;

    > li.option {
      height: 100%;
      flex: 1 0 0;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: var(--border-rad-lg);
      color: var(--color-text-5);
      user-select: none;
      font-size: 0.8125rem;

      &.selected {
        font-weight: 700;
        background-color: var(--color-bg-8);
        box-shadow: var(--shadow-surround-sharp-down);
        font-size: 0.875rem;
        color: var(--color-text-4);
      }

      &:hover:not(.selected) {
        background-color: var(--color-bg-4);
      }

      &:active:not(.selected) {
        color: var(--color-text-0);
      }

      &:not(:last-of-type) {
        margin-right: 0.25rem;
      }
    }
  }
</style>
