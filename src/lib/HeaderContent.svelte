<!-- HeaderContent.svelte -->
<script lang="ts">
</script>

<div>
  <ul>
    <li><a class="text-gray-700 hover:text-gray-900" href="/cv">CV</a></li>
    <li>
      <a class="text-gray-700 hover:text-gray-900" href="/contact">Contact</a>
    </li>
  </ul>
</div>

<style>
  div {
    display: grid;
    grid-template-columns: 1fr auto;
    grid-area: ". content";

    gap: 1rem;
    padding-right: 40px;
  }

  ul {
    grid-column-start: -1;
  }

  ul li {
    display: inline;
  }

  li {
    padding: 10px;
  }
</style>
