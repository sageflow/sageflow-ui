<template lang="pug">
#sidebar-settings
  //- Sidebar Header.
  sidebar-header.sidebar-header(name="settings", iconName="settings")

  //- Main content.
  .main

</template>

<script>
  import SidebarHeader from "@/components/layout/SidebarHeader"
  import SearchBar from "@/components/ui/SearchBar"
  import Collection from "@/components/ui/Collection"

  export default {
    components: {
      SidebarHeader,
      SearchBar,
      Collection,
    },
    setup() {},
  }
</script>

<style lang="scss" scoped>
  #sidebar-settings {
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
