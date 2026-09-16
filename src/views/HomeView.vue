<template>
  <div>
    <main>
      <NavbarC />
    </main>
    <div>
    </div>
    <div>
      <TeamSlection />
    </div>
  </div>
</template>

<script>
import NavbarC from '@/components/NavbarC.vue';
import TeamSlection from '@/components/TeamSlection.vue';
export default {
  name: 'HomeView',
  components: {
    NavbarC,
    TeamSlection
  }
}
</script>

<style>
main {
  min-height: 0vh;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0.039), rgba(0, 0, 0, 1));
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
