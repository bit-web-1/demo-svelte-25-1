<script>
    let { quote } = $props();
</script>

<div>
    <blockquote cite={quote.citeUrl}>
      <p>
        {quote.quoteText}
      </p>
    </blockquote>
    <p>—{quote.author}, <cite>{quote.publication}</cite></p>
  </div>

<style>
    
</style>