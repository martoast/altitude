<template>
  <img class="VuetifyLogo" alt="Vuetify Logo" src="~/assets/penlogo.png" />
</template>

<style>
.VuetifyLogo {
  width: 50px;
  height: 50px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
