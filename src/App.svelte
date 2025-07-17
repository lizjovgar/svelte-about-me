<script>
  let name = "Lizbeth Jovanna"; // Change this to your name
  let bio = "4th year Information Systems major specializing in Data Analytics";
  let hobbies = ["Exploring", "Running", "Resting", "Eating"]; // List some hobbies
  //let KWKhistory = ["2020: Mobile App Development", " 2021: Web Development", " 2025: Data Storytelling Challenge"]


  import ImageCard from "./lib/ImageCard.svelte";
  
  let cardData = [
    {
      image:
        "https://i.imgur.com/gFWwTTc.jpeg",
      title: "Music",
      description:
        "I love listening to music, going to concerts, and collecting vinyls. This is my with my favorite artist, Omar Apollo!",
    },
    {
      image: "https://i.imgur.com/LTzQFxq.jpeg",
      title: "Watching TV Shows & Movies",
      description: "Above is a picture of my boyfriend and I on a location where my favorite show, The Good Place, was filmed!",
    },
    {
      image: "https://i.imgur.com/rDHmAIG.jpeg",
      title: "Pucca",
      description:
        "My first cat ever, Pucca!≽^•⩊•^≼",
    },
  ];

</script>

<style>
  h1 {
    color: #000407;
    font-family: Gelasio;
  }

  p {
    color: rgb(49, 33, 0);
    font-family: Gelasio;
  }

  h2 {
    color: rgb(49, 33, 0);
    font-family: Gelasio;
  }

  h3 {
    color: rgb(49, 33, 0);
    font-family: Gelasio;
  }

  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #403500;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }

  .card-container {
    display: flex;
    flex-direction: column;
    align-items: center;     
    gap: 20px;              
    margin-top: 20px;
  }
</style>

<div class="container">
  <h1>⋆⭒˚.⋆About Me⋆⭒˚.⋆</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>{bio}</p>
  <p><strong>My KWK History:</strong></p>
  <p><strong>2020:</strong>  Mobile App Development</p>
  <p><strong>2021:</strong>  Web Development</p>
  <p><strong>2025:</strong> Data Storytelling Challenge</p>

  <h2>My Hobbies</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>

<h2>Some of My Favorite Things</h2>
<div class="card-container">
  {#each cardData as { image, title, description }}
    <ImageCard {image} {title} {description} />
  {/each}
</div>

<h2>⋆⭒˚.⋆Playlist of my favorite songs⋆⭒˚.⋆</h2>

<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/6NGsnAwfi9qTPUT5vTWP28?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>