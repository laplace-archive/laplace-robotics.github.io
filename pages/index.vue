<template>
  <v-app>
    <v-main>
      <v-container fluid fill-height>
        <v-row class="pa-2 fill-height" justify="center" align="center">
          <a class="flex-grow-1" href="https://github.com/laplace-robotics" target="_blank">
            <v-img
              contain
              src="/laplace-logo-name.svg"
              transition="slide-fade"
              v-ripple
            />
          </a>
        </v-row>
      </v-container>
    </v-main>

    <v-footer outlined padless>
      <v-row justify="center" no-gutters>
        <strong class="text-center secondary--text font-weight-light">
          {{ new Date().getFullYear() }} - 
          <a class="secondary--text font-weight-light" href="https://github.com/laplace-robotics" target="_blank">
            Github
          </a> -
          <a class="secondary--text font-weight-light" href="mailto:rae@laplacerobotics.com" target="_blank">
            Contact Us
          </a>
        </strong>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>

export default {
  components: {
  }
}
</script>

<style>
/* Hide scrollbars in html */
html {
  overflow: hidden !important;
}

v-main {
  overflow: auto;
}

.slide-fade-enter-active, .slide-fade-leave-active {
  transition: all 2s ease;
}

.slide-fade-enter, .slide-fade-leave-to {
  transform: translateX(-200px);
  opacity: 0;
}

.blink {
  animation: blinking 2 s alternate ease-in-out infinite none running;
}

@keyframes blinking {
  0%{opacity: 1;}
  100%{opacity: 0.75;}
}

</style>
