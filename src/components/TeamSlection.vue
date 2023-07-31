<template>
  <main>
    <section id="about">
      <div class="home">
        <div class="home container d-flex align-items-center justify-content-center">
          <div class="row">
            <div class="col landing-text text-dark m-auto text-center" style="padding-top: 4rem;">
              <div>
                <h2 class="text-center text-white" id="random-title">
                  SQUAD RANDOMIZER
                </h2>
                <div class="container d-flex justify-content-center p-3">
                  <div class="row">
                    <div class="col-12 col-md-6">
                      <input type="text" v-model="playerName" placeholder="Enter Player Name" />
                    </div>
                    <div class="col-12 col-md-6">
                      <input type="text" v-model="playerImage" placeholder="Enter player image URL" />
                    </div>
                  </div>
                </div>
                <div class="container d-flex justify-content-center">
                  <ul class="btns">
                    <li>
                      <button class="btn btn-dark p-3" @click="addPlayer">
                        Add Player <i class="fa-solid fa-circle-plus"></i>
                      </button>
                    </li>
                    <li>
                      <button class="btn btn-dark p-3" @click="randomizeTeams">
                        Randomize Teams <i class="fa-solid fa-infinity"></i>
                      </button>
                    </li>
                    <li>
                      <button class="btn btn-dark p-3" @click="clearPlayers">
                        Clear Players <i class="fa-solid fa-trash"></i>
                      </button>
                    </li>
                  </ul>
                </div>
                <h3 class="text-center mt-1">Players Available:</h3>
                <ol id="playersList" class="d-flex flex-wrap justify-content-center">
                  <li v-for="player in players" :key="player.name">
                    {{ player.name }}
                  </li>
                </ol>
                <div class="container">
                  <div class="row text-center teams">
                    <div class="col-12 col-sm-6 col-md-6 col-lg-6 border">
                      <h3 class="p-2 border-bottom">TEAM 1:</h3>
                      <ol class="text-center" id="team1">
                        <li v-for="(player, index) in teams.team1" :key="index">
                          {{ player.name }}
                        </li>
                      </ol>
                    </div>
                    <div class="col-12 col-sm-6 col-md-6 col-lg-6 border">
                      <h3 class="p-2 border-bottom">TEAM 2:</h3>
                      <ol class="text-center" id="team2">
                        <li v-for="(player, index) in teams.team2" :key="index">
                          {{ player.name }}
                        </li>
                      </ol>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      playerName: "",
      playerImage: "",
      players: [],
      teams: {
        team1: [],
        team2: [],
      },
    };
  },
  methods: {
    addPlayer() {
      if (this.playerName !== "") {
        this.players.push({ name: this.playerName, image: this.playerImage });
        this.playerName = "";
        this.playerImage = "";
      }
    },
    randomizeTeams() {
      if (this.players.length < 10) {
        alert("Please add at least 10 players to the list.");
        return;
      }

      this.teams.team1 = [];
      this.teams.team2 = [];

      let randomizedPlayers = this.shuffleArray(this.players.slice());

      for (let i = 0; i < 10; i++) {
        let player = randomizedPlayers[i];
        if (i < 5) {
          this.teams.team1.push(player);
        } else {
          this.teams.team2.push(player);
        }
      }
    },
    shuffleArray(array) {
      let currentIndex = array.length,
        temporaryValue,
        randomIndex;

      while (0 !== currentIndex) {
        randomIndex = Math.floor(Math.random() * currentIndex);
        currentIndex -= 1;

        temporaryValue = array[currentIndex];
        array[currentIndex] = array[randomIndex];
        array[randomIndex] = temporaryValue;
      }

      return array;
    },
    clearPlayers() {
      this.players = [];
      this.teams.team1 = [];
      this.teams.team2 = [];
    },
  },
};
</script>

<style scoped>
main {
  min-height: 100vh;
  background: linear-gradient(to top, rgba(255, 255, 255, 0.039), rgba(0, 0, 0, 1)),
    url(https://i.postimg.cc/FzLx4vxt/fifa-background-tqq9pxlhzeue8u6w.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: auto;
}

.btn {
  padding: 1rem;
  border-radius: 2px;
}

.btn:hover {
  box-shadow: 3px 5px rgb(140, 140, 140);
}

.btns {
  display: flex;
  list-style: none;
  gap: 2rem;
  padding: 0;
}

input[type="text"] {
  padding: 10px;
  text-align: center;
  border: 1px solid black;
  box-shadow: 3px 5px rgb(195, 195, 195);
}

#playersList {
  display: flex;
  gap: 5rem;
  justify-content: center;
  font-weight: 900;
}

.home {
  margin-left: 4rem;
}

@media screen and (max-width: 768px) {
  .home {
    margin-left: 0;
  }

  #playersList {
    display: block;
    margin: auto;
    text-align: center;
  }

  .row {
    display: block;
    margin-left: 0rem !important;
  }

  .btns {
    display: block;
  }

  .btn {
    margin-top: 1rem;
  }
}
</style>