<template>
  <div class="outer-container">
    <div class="project" id="froyo">
      <div class="left">
        <img src="../assets/code_demos/froyo/FroyoStartScreen.png" id="froyo-start"/>
        <img src="../assets/code_demos/froyo/FroyoGameScreen.png" id="froyo-game"/>
      </div>
      <div class="middle">
        <h1>FROYO GAMES</h1>
        <ul class="code-description">
          <li>A Java application that allows users to play Othello, Checkers, and Connect 4</li>
          <li>Three modes for each game
            <ul>
              <li class="first-sub">One Player versus an AI that uses minmax</li>
              <li>Two Player local, in which the same input device and computer is used by both players</li>
              <li class="last-sub">Two Player online, in which players can play against each other different devices (uses Firebase, now deprecated)</li>
            </ul>
          </li>
          <li>Users can choose between three languages for the application when first opening it</li>
          <li>Worked on a team of five across various time zones, using Scrum methodology</li>
          <li>Used an MVC project structure while following SOLID design principles and incorporating OOP design patterns</li>
        </ul>
      </div>
      <div class="right">
        <img src="../assets/code_demos/froyo/FroyoOthello.png" id="froyo-othello"/>
        <img src="../assets/code_demos/froyo/FroyoCheckers.png" id="froyo-checkers"/>
        <img src="../assets/code_demos/froyo/FroyoConnect4.png" id="froyo-connect"/>
      </div>
    </div>
    <div class="project" id="amazon">
      <div class="left">
        <img src="../assets/code_demos/amazon/mini_amazon_home.png" id="amazon-home"/>
      </div>
      <div class="middle">
        <h1>MINI AMAZON</h1>
        <ul class="code-description">
          <li>A mock online shopping platform that allows for users to buy and sell items</li>
          <li>Includes a number of features, such as database search functions, buyer and seller accounts, leaving reviews for items, querying by item category, “cart” functionality, and “warehouse” functionality that estimated shipping times</li>
          <li>Used HTML, CSS, Python, Flask, and SQLAlchemy</li>
          <li>Worked on a team of five, with myself focusing on the ability to create a “seller” account that can add listings for other users to purchase</li>
        </ul>
      </div>
      <div class="right">
        <img src="../assets/code_demos/amazon/mini_amazon_seller.png" id="amazon-seller"/>
      </div>
    </div>
    <div class="project" id="french">
      <div class="left">
        <img src="../assets/code_demos/flashcards/flash_card_maker.png" id="french-program"/>
      </div>
      <div class="middle">
        <h1>FRENCH FLASH CARD MAKER</h1>
        <ul class="code-description">
          <li>A Python application that takes in French text and creates a flash card deck with the English translations</li>
          <li>Uses Tkinter for the GUI and the WordReference API for translations</li>
          <li>Flash card deck is a .txt document formatted to be read by the Anki flashcard program</li>
        </ul>
      </div>
      <div class="right">
        <img src="../assets/code_demos/flashcards/flash_card_doc.png" id="french-txt"/>
      </div>
    </div>
    <div class="project" id="spotify">
      <div class="left">
        <img src="../assets/code_demos/spotify/spotify_nouvelles.png" id="spotify-nouvelles"/>
      </div>
      <div class="middle">
        <h1>SPOTIFY SORTER</h1>
        <ul class="code-description">
          <li>A Python script that sorts songs into playlists based on their genre</li>
          <li>Uses the Spotify API, specifically Spotipy Python library</li>
          <li>I wanted to create a method for finding and sorting new music, so whenever I hear a new song that I like, or one is recommended to me, I add it to my “new” playlist (”nouvelles” in French), and every so often I can run the script to go through the “new” playlist and do the following:
            <ul>
              <li class="first-sub">Add the song to one or multiple genre playlists based on the metadata provided through the Spotify API</li>
              <li>Add the song to my “liked” songs</li>
              <li class="last-sub">Remove the song from the “new” playlist in order to start fresh after sorting</li>
            </ul>
          </li>

        </ul>
      </div>
      <div class="right">
        <img src="../assets/code_demos/spotify/spotify_added.png" id="spotify-added"/>
      </div>
    </div>


  </div>
</template>

<script>
export default {

}
</script>


<style>

.project {
  margin: auto;
  display: flex;
  padding: 2em
}

.left {
  text-align: left;
  margin: auto;
}
.middle {
  padding-left: 3em;
  padding-right: 3em;
}
.right {
  text-align: left;
  margin: auto;
}



.code-description {
  text-align: left;
}

.first-sub {
  padding-top: 0.5em;
}

.last-sub {
  padding-bottom: 0em;
}
#froyo-start {
  height: 6em;
}
#froyo-game {
  height: 13em;
}

#froyo-othello {
  height: 12em;
}
#froyo-checkers {
  height: 12em;
}
#froyo-connect {
  height: 12em;
}
#amazon-home {
  height: 10em;
}
#amazon-seller {
  height: 10em;
}
#french-program {
  height: 13em;
}
#french-txt {
  height: 15em;
}
#spotify-nouvelles {
  height: 15em;
}
#spotify-added {
  height: 15em;
}

</style>