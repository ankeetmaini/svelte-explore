<script>
  const getDog = async () => {
    const dog = await fetch(
      "https://api.thedogapi.com/v1/images/search?size=med&mime_types=jpg&format=json&has_breeds=true&order=RANDOM&page=0&limit=1"
    ).then(r => r.json());
    return dog;
  };
  let dog = getDog();

  const getNew = () => {
    dog = getDog();
  };
</script>

<style>
  img {
    height: 200px;
    width: 200px;
    object-fit: contain;
  }
</style>

<h1>Say hi!</h1>
<h4>
  <button on:click={getNew}>Get NEXT!</button>
</h4>
{#await dog}
  loading...
{:then data}
  <div>
    <img src={data[0].url} alt="doggo" />
  </div>

{:catch}
  <h5>Sorry, couldn't fetch doggo</h5>
{/await}
