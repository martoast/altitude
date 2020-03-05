<template>
  <img class="logo" alt="Logo" src="~/assets/altitudelogo.png" />
</template>

<style>
.Logo {
  width: 100px;
  height: 100px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
