<script>
    import Footer from "$lib/Footer.svelte";
    import Card from "$lib/Card.svelte";
    import Quote from "$lib/Quote.svelte";

    let bananas =  {
        quoteText: "Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.",
        author: "Aldous Huxley",
        publication: "Brave New World",
        citeUrl: "https://www.huxley.net/bnw/four.html"
        }

</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Quote quote={bananas} />

<section class="card-grid">
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
</section>
<Footer />

<style>
    :global(body) {
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }
    .card-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    }
</style>