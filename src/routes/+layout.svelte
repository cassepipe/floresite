<script>
  import "../app.css";
</script>

<div id="page" class="h-screen">
  <nav id="sidebar">Sidebar</nav>
  <nav id="header">Header</nav>
  <div id="main">Main</div>
</div>

<!-- Using CSS directly for the grid layout instead of using Tailwind classes -->
<style>
  #page {
    /* Margins and gaps*/
    margin-left: 2rem;
    margin-right: 0px;
    margin-top: 2rem;
    margin-bottom: 0px;
    gap: 1.5rem;

    /* Grid Layout */
    display: grid;
    grid-template-columns: 1fr 5fr;
    grid-template-rows: 30px 1fr;
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
