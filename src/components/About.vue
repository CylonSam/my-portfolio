<template>
  <div class="about-main">
    <h1 class="text-6xl title">Hi, I'm Sam.</h1>
    <p class="content-text text-xl font-thin">
      I'm a fullstack web developer and hot dog enthusiast based in Belém-PA. My
      favorite programming language is Python, I learned it when I was 16 years
      old and just fell in love with the language of the snakesssss. Later when
      I got to college I learned the ways of the C (-ith), C++ and Java (eww).
    </p>
    <p class="content-text text-xl font-thin">
      I'm majoring in Computer Engineering and I'm also a dev inturn in my
      college's library, where I learned many other things like PHP, Javascript,
      Vue.js, Node.js, Linux server thingies and to never run the command 'sudo
      iptables -F'. As for my hobbies, I like to play games, read books, watch
      tv shows and play the guitar (poorly).
    </p>
    <p class="content-text text-xl font-thin">
      Feel free to judge my personal taste:
    </p>

    <div class="lists flex flex-wrap justify-around">
      <div class="card rounded flex flex-col">
        <p class="card-title">STEAM</p>
        <p class="card-text">Yeah, I like a lil bit of rpg</p>
        <button class="card-button rounded">
          Judge
          <font-awesome-icon
            class="card-button-icon"
            :icon="['fab', 'steam-square']"
          ></font-awesome-icon>
        </button>
      </div>
      <div class="card rounded flex flex-col">
        <p class="card-title">SPOTIFY</p>
        <p class="card-text">Prepare to be disapointed</p>
        <button class="card-button rounded">
          Judge
          <font-awesome-icon
            class="card-button-icon"
            :icon="['fab', 'spotify']"
          ></font-awesome-icon>
        </button>
      </div>
      <div class="card rounded flex flex-col">
        <p class="card-title">IMDB</p>
        <p class="card-text">Mainstream with a touch of mainstream</p>
        <button class="card-button rounded">
          Judge
          <font-awesome-icon
            class="card-button-icon"
            :icon="['fab', 'imdb']"
          ></font-awesome-icon>
        </button>
      </div>
      <div class="card rounded flex flex-col">
        <p class="card-title">BOOKS</p>
        <p class="card-text">Basically sci-fi and romance</p>
        <button class="card-button rounded">
          Judge
          <font-awesome-icon
            class="card-button-icon"
            :icon="['fab', 'goodreads']"
          ></font-awesome-icon>
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
.about-main {
  background: #f0f5f9;
  padding: 7% 6% 2%;
  width: 100%;
}
.title {
  margin-bottom: 0.4em;
  font-family: "Oswald", sans-serif;
  color: #1e2022;
}

.content-text {
  font-family: "Cormorant Garamond", serif;
  color: #1e2022;
  margin-top: 0.5em;
}

.lists {
  /* margin-top: 3%; */
  margin: 3% 8% 0;
}

.card {
  width: 10rem;
  height: 10.5rem;
  padding: 1%;
  background: #c9d6df;
}

.card-title {
  color: #1e2022;
  font-family: "Oswald", sans-serif;
  font-weight: bold;
  font-size: 1.3rem;
}

.card-text {
  font-family: "Oswald", sans-serif;
  color: #1e2022;
}

.card-button {
  margin-top: 2rem;
  width: 100%;
  height: 2rem;
  background: #1e2022;
  color: #c9d6df;
}

.card-button-icon {
}
</style>

