<template lang="pug">
#sidebar-developer
  //- Sidebar Header.
  sidebar-header.sidebar-header(name="developer")

  //- Main content.
  .main
</template>

<script>
  import SidebarHeader from "@/components/layout/SidebarHeader"
  export default {
    components: {
      SidebarHeader,
    },
    setup() {},
  }
</script>

<style lang="scss" scoped>
  #sidebar-developer {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;

    > .main {
      flex-grow: 1;
      background-color: var(--color-bg-8);
    }
  }
</style>
