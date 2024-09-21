<script>
  import "../app.css";
  import SidebarContent from "$lib/SidebarContent.svelte";
  import HeaderContent from "$lib/HeaderContent.svelte";
</script>

<div id="page" class="h-screen overflow-hidden">
  <div id="sidebar" class="bg-lime-600 p-2">
    <SidebarContent></SidebarContent>
  </div>

  <div id="header">
    <HeaderContent></HeaderContent>
  </div>

  <div id="main" class="overflow-scroll">
    <slot></slot>
  </div>
</div>

<!-- Using CSS directly for the grid layout instead of using Tailwind classes -->
<style>
  :root {
    --header-height: 50px;
  }

  #page {
    /* Margin must be 0 for overflow: hidden to work; */
    margin: 0px;

    /* Grid Layout */
    display: grid;
    grid-template-columns: 1fr 6fr;
    grid-template-rows: var(--header-height) 1fr;
    grid-template-areas:
      " sidebar header "
      " sidebar main   ";
  }
  #sidebar {
    grid-area: sidebar;
    margin-left: 30px;
    margin-top: var(--header-height);
  }
  #header {
    grid-area: header;
  }
  #main {
    grid-area: main;
  }
</style>
