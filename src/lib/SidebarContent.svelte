<!-- SidebarContent.svelte -->
<script lang="ts">
  const links = ["Programme", "Éditions", "Trucmuche"];
</script>

<a href="/" aria-label="Home">
  <img
    src="https://images.photowall.com/products/44761/van-gogh-vincent-self-portrait.jpg?h=250"
    alt="Arty me"
  />
</a>

<ul>
  {#each links as link}
    <li>
      <a
        class="text-gray-700 hover:text-gray-900"
        href={link
          .normalize("NFD")
          .replace(/[\u0300-\u036f]/g, "")
          .toLowerCase()}>{link}</a
      >
    </li>
  {/each}
</ul>

<style>
  ul {
    margin-top: 0px;
    margin-bottom: 0px;
  }

  a {
    margin-top: 0px;
    margin-bottom: 0px;
  }
</style>
