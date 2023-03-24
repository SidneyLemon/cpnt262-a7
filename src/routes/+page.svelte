<script>
  import { animals } from "/src/lib/data.js";
</script>

<main>
  <section>
    {#each animals as animals}
      <article class="card">
        <img
          src="/{animals.images}"
          width="200"
          height="200"
          alt="animal images"
        />
        <a href={animals.url} target="_blank">
          <h1>{animals.title}</h1>
          <p>{animals.description}</p>
        </a>
      </article>
    {/each}
  </section>
</main>

<style>
  section {
    padding: 10rem;
    display: flex;
    justify-content: center;
    gap: 2rem;
  }
  article {
    border: 1px solid black;
    background-color: white;
    border-radius: 3rem;
    padding: 5rem;
    text-decoration: none;
    width: 100%;
  }
  article:hover {
    background-color: rgb(240, 236, 236);
    box-shadow: black;
  }
</style>
