<script>
    import Footer from "$lib/Footer.svelte";
    import Card from "$lib/Card.svelte";
    import Quote from "$lib/Quote.svelte";

    let quotes = [
        {
            quoteText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet, totam qui nulla accusantium incidunt odit quo nihil voluptatem voluptatum officiis, eum fugiat consectetur? Inventore, sed dicta sunt placeat dolore molestiae!",
            author: "Cicero",
            publication: "Lorem Ipsum",
            citeUrl: "https://www.huxley.net/bnw/four.html"
        },
        {
            quoteText: "Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.",
            author: "Aldous Huxley",
            publication: "Brave New World",
            citeUrl: "https://www.huxley.net/bnw/four.html"
        },
        {
            quoteText: "I'm Batman",
            author: "Batman",
            publication: "Dark Knight",
            citeUrl: "https://www.huxley.net/bnw/four.html"
        },
        {
            quoteText: "It is hard to fail but it is worse never to have tried to succeed.",
            author: "Theodore Roosevelt",
            publication: "",
            citeUrl: "https://www.shutterfly.com/ideas/best-quotes-of-all-time/?msockid=3c99785b330c66ae0c8f6db0323e67db"
        }
    ];

    let cards = [
        {
            title: "My Card",
            user: {
                userName: "@doggo",
                img: "https://picsum.photos/id/237/200/200"
            },
            info: "information here"
        },
        {
            title: "My Other Card",
            user: {
                userName: "@doggo2",
                img: "https://picsum.photos/id/237/200/200"
            },
            info: "More kinds of information here"
        }
    ]
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

{#each quotes as quote}
    <Quote {quote} />
{/each}

<section class="card-grid">
    {#each cards as card}
        <Card cardData={card} />
    {/each}
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