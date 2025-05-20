<script>
  import SiteHeader from "$lib/SiteHeader.svelte";

  let { children } = $props();
</script>

<!-- Include the main heading and the navigation -->
<SiteHeader />

<!-- This is where the page content will go -->
{@render children()}

<style>
</style>
