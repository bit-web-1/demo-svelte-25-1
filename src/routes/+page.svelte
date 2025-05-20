<script>
  import Card from "$lib/Card.svelte";

  let cards = [
    {
      title: "My Card",
      user: {
        userName: "@doggo",
        img: "https://picsum.photos/id/237/200/200",
      },
      info: "information here",
    },
    {
      title: "My Other Card",
      user: {
        userName: "@doggo2",
        img: "https://picsum.photos/id/237/200/200",
      },
      info: "More kinds of information here",
    },
  ];
</script>

<section class="card-grid">
  {#each cards as card}
    <Card cardData={card} />
  {/each}
</section>

<style>
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  }
</style>
