<!-- src/lib/ImageCard.svelte -->

<script>
  export let image;  // Image URL prop
  export let title;  // Title prop
  export let description;  // Description prop
</script>

<style>
  .card {
    background-color: plum;
    border: 1px solid #ddd;
    border-radius: 10px;
    overflow: hidden;
    width: 250px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin: 20px;
    text-align: center;
    transition: transform 0.2s ease-in-out;
  }

  .card img {
    width: 100%;
    height: auto;
    border-radius: 5px;
  }

  .card-content {
    padding: 15px;
  }

  .card-title {
    font-size: 1.5em;
    color: #f7f5f5;
    margin: 0 0 10px 0;
  }

  .card-description {
    font-size: 1em;
    color: #f7f5f5;
    margin: 0;
  }

  .card:hover {
    transform: scale(1.05);
    cursor: pointer;
  }

</style>

<div class="card">
  <img src={image} alt={title} />
  <div class="card-content">
    <h2 class="card-title">{title}</h2>
    <p class="card-description">{description}</p>
  </div>
</div>
