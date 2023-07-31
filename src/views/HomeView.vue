<template>
  <div>
    <main>
      <NavbarC />
      <section id="about">
        <div class="home">
          <div class="home container d-flex align-items-center justify-content-center">
            <div class="row">
              <div class="col landing-text text-light" style="padding-top: 19rem; ">
                <h1>WAR ON THE TURF <span class="comma">,</span> SPLITTING THE PATHS</h1>
                <button class="btn btn-dark"><a style="text-decoration: none; color: white;"
                    href="#cardsPage">PROCEED</a></button>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
    <div>
      <PlayerCards />
    </div>
    <div>
      <TeamSlection />
    </div>
  </div>
</template>

<script>
import NavbarC from '@/components/NavbarC.vue';
import PlayerCards from '@/components/PlayerCards.vue';
import TeamSlection from '@/components/TeamSlection.vue';
export default {
  name: 'HomeView',
  components: {
    NavbarC,
  PlayerCards,
    TeamSlection
  }
}
</script>

<style>
main {
  min-height: 100vh;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0.039), rgba(0, 0, 0, 1)), url(https://i.postimg.cc/FzLx4vxt/fifa-background-tqq9pxlhzeue8u6w.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: auto;
}

@media screen and (max-width: 768px) {
  .comma {
    display: none;
  }
}
</style>
