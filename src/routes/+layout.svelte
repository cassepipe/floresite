<script>
  import "../app.css";
  import SidebarContent from "$lib/SidebarContent.svelte";
  import HeaderContent from "$lib/HeaderContent.svelte";
</script>

<div id="page" class="h-screen">
  <div id="sidebar" class="bg-lime-600 p-2">
    <SidebarContent></SidebarContent>
  </div>

  <div id="header">
    <HeaderContent></HeaderContent>
  </div>

  <div id="main">
    <slot></slot>
  </div>
</div>

<!-- Using CSS directly for the grid layout instead of using Tailwind classes -->
<style>
  #page {
    /* Margins and gaps*/
    margin-left: 2rem;
    margin-right: 20px;
    margin-top: 2rem;
    margin-bottom: 0px;
    gap: 1.5rem;

    /* Grid Layout */
    display: grid;
    grid-template-columns: 1fr 6fr;
    grid-template-rows: 40px 1fr;
    grid-template-areas:
      " sidebar header "
      " sidebar main   ";
  }
  #sidebar {
    grid-area: sidebar;
  }
  #header {
    grid-area: header;
  }
  #main {
    grid-area: main;
  }
</style>
