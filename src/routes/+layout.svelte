<script>
  import Footer from "$lib/Footer.svelte";
  import SiteHeader from "$lib/SiteHeader.svelte";

  let { children } = $props();
</script>

<!-- Include the main heading and the navigation -->
<SiteHeader />

<!-- This is where the page content will go -->
{@render children()}

<!-- The website footer -->
<Footer />

<style>
  :global(body) {
    font-family:
      system-ui,
      -apple-system,
      BlinkMacSystemFont,
      "Segoe UI",
      Roboto,
      Oxygen,
      Ubuntu,
      Cantarell,
      "Open Sans",
      "Helvetica Neue",
      sans-serif;
  }
</style>
