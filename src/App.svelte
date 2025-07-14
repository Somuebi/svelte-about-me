<script>
  import ImageCard from "./lib/ImageCard.svelte"

  let name = "Mmesoma Onwusika" ; // Change this to your name";
  let favoriteNumber = 12; // Change this to your favorite number
  let bio = "I am from lagos, Nigeria. Currently, I am a student at Worcester Polytechnic Institue majoring in Computer Science.  I started coding in fifth grade with a basic HTML page. Afterwards, I fully got into programming and started learning Python in school. I spent a while learning python making mini projects. While in high school in the USA. I learnt Java and took both AP Computer Science Principles and AP Computer Science A. In the summer before my senior year of high school I did the Kode WIth Klossy Web Development camp and gained a good grasp on HTML, CSS, and JavaScript. Now I have learned C, C++ and Racket.";
  let hobbies = ["Cooking", "Reading", "Coding", "Watching Shows"]; // List some hobbies
  let cardData = [
    {
      image:
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcStpHpXYugLkFRTzIYH_h_N-kj71Xicw-4fFQ&s",
      title: "Coding",
      description:
        "I love solving problems and writing code to build cool things.",
    },
    {
      image: "https://i0.wp.com/wearerestless.org/wp-content/uploads/2021/02/Reading-scaled.jpg?resize=1155%2C770&ssl=1",
      title: "Reading",
      description: "I love exploring new words with books",
    },
    {
      image: "https://media.istockphoto.com/id/1440399157/photo/international-airport-terminal-asian-beautiful-woman-with-luggage-and-walking-in-airport.jpg?s=612x612&w=0&k=20&c=RqmI0KG_pnEb_GmWLC6pY5MoV75JBt1nU1L9dStkJys=",
      title: "Traveling",
      description:
        "I enjoy exploring new cultures and learning from the world around me.",
    },
    {
      image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpnO8URXU2jdQ9YFNUDBaGpTFVh2yW8kOpug&s",
      title: "Cooking",
      description: "I love cooking and making new food",
    }
  ];
</script>

<style>
  h1 {
    color: #2c3e50;
    font-family: Arial, sans-serif;
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
    background-color: #3498db;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
</style>

<div class="container">
  <h1>About Me</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>Hobbiess</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
    <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>
