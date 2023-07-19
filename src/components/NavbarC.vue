<template>
  <nav class="navbar navbar-expand-lg sticky">
    <div class="container-fluid bg-transparent">
      <!-- <a href="/"><img style="width: 4rem;" src="https://i.postimg.cc/fb5tHqQV/fifa23-logo-0.png"></a> -->
      <button class="navbar-toggler text-bg-light" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse " id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active text-dark" aria-current="page" href="/" style="font-size: 30px;">SPLIT THE SQUAD</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'NavbarC'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Alegreya+Sans+SC:wght@700&display=swap');

nav {
  /*
  background-color: transparent;
  backdrop-filter: blur(5px);
  */
  opacity: 0.8500000238418579;
  background: #FFF;
  box-shadow: 0px 4px 4px 0px #000;
}

.navbar-toggler,
.navbar-toggler-icon {
  color: #000000;
}

.navbar-toggler {
  border-color: rgb(0, 0, 0);
}
</style>