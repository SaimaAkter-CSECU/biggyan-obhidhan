<template>
  <Header class="container">
    <nav
      class="navbar navbar-expand-lg bg-white"
      v-bind:class="scrollPosition > 120 ? 'fixed-top nav-shrink' : ''"
    >
    <div class="container">
        <a class="navbar-brand" href="#">
            <img :src="logo" class="img-fluid" alt="Biggan Obhidhan" />
        </a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
            <!-- <span class="navbar-toggler-icon"></span> -->
            <span class="material-icons-outlined text-hover">menu</span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto mt-3">
                <li class="nav-item px-2">
                    <a class="nav-link active" aria-current="page" href="#">Home</a>
                </li>
                <li class="nav-item px-2">
                    <a class="nav-link" href="#facility">Features</a>
                </li>
                <li class="nav-item px-2">
                    <a class="nav-link" href="#">About</a>
                </li>
                <li class="nav-item px-2">
                    <a class="nav-link" href="#">Team</a>
                </li>
                <li class="nav-item px-2">
                    <a class="nav-link" href="#">Instructors</a>
                </li>
                <li class="nav-item px-2">
                    <a class="nav-link" href="#contact">Contact</a>
                </li>
            </ul>
        </div>
      </div>
    </nav>
  </Header>
</template>

<script>
import logo from "../assets/biggyan-main-logo.png";

export default {
  name: "HeaderSection",
  data: () => ({
    logo: logo,
    isSticky: false,
    scrollPosition: null,
    w: window.innerWidth,
  }),
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },
};
</script>
