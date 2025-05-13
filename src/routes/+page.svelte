<script>
    import Footer from "$lib/Footer.svelte";
    import Card from "$lib/Card.svelte";
    import Quote from "$lib/Quote.svelte";

    let lorem =  {
        quoteText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet, totam qui nulla accusantium incidunt odit quo nihil voluptatem voluptatum officiis, eum fugiat consectetur? Inventore, sed dicta sunt placeat dolore molestiae!",
        author: "Cicero",
        publication: "Lorem Ipsum",
        citeUrl: "https://www.huxley.net/bnw/four.html"
        }

    let huxley =  {
        quoteText: "Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.",
        author: "Aldous Huxley",
        publication: "Brave New World",
        citeUrl: "https://www.huxley.net/bnw/four.html"
        }

    let batman =  {
        quoteText: "I'm Batman",
        author: "Batman",
        publication: "Dark Knight",
        citeUrl: "https://www.huxley.net/bnw/four.html"
        }

</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Quote quote={huxley} />
<Quote quote={batman} />
<Quote quote={lorem} />

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