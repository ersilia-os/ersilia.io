<template>
  <div class="connect">

    <transition-group name="fade">
      <div class="connect__slide" key=1 v-show="activeSlide == 0"><g-image class="connect__logos" src="~/assets/images/Ersilia_Doctor_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Doctor" /></div>
      <div class="connect__slide" key=2 v-show="activeSlide == 1"><g-image class="connect__logos" src="~/assets/images/Ersilia_Publications_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Publications" /></div>
      <div class="connect__slide" key=3 v-show="activeSlide == 2"><g-image class="connect__logos" src="~/assets/images/Ersilia_Bacteria_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Bacteria" /></div>
      <div class="connect__slide" key=4 v-show="activeSlide == 3"><g-image class="connect__logos" src="~/assets/images/Ersilia_Computer_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Computer" /></div>
      <div class="connect__slide" key=5 v-show="activeSlide == 4"><g-image class="connect__logos" src="~/assets/images/Ersilia_Drug_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Drug" /></div>
      <div class="connect__slide" key=6 v-show="activeSlide == 5"><g-image class="connect__logos" src="~/assets/images/Ersilia_Globe_Green-01.png" width="1180" blur="10" retina="true" alt="Ersilia Globe" /></div>
    </transition-group>

    <g-image class="connect__main" src="~/assets/images/empty-background.png" width="1180" blur="0" retina="true" alt="Empty background" />

  </div>
</template>

<script>
export default {
  data() {
    return {
      activeSlide: 0
    }
  },

  mounted () {
    (($vm) => {
      (function animate () {
        $vm._counter = setTimeout(() => {
          $vm.activeSlide = ($vm.activeSlide + 1) % 3
          requestAnimationFrame(animate)
        }, 1500)
      })()
    })(this)
  },

  destroyed () {
    clearTimeout(this._counter)
  }
}
</script>

<style lang="scss">

.fade-enter-active, .fade-leave-active {
  transition: opacity 1s, transform 1s;
  transform: translateY(0);
}

.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(5px);
}

.connect {
  position: relative;

  img {
    margin: 0;
    width: 100%;
  }

  svg,
  &__slide,
  &__logos {
    width: 100%;
    left:0;
    top:0;
    height: 100%;
    position: absolute;
  }
  svg
   path {
    stroke-linecap: round;
    stroke-dasharray: 0.5 30;
    stroke: var(--primary-color-dark);
    animation: DotsAnim 600ms linear infinite;
    opacity: .6;
  }

}

@keyframes DotsAnim{
  100% {
      stroke-dashoffset: -30;
  }
}
</style>
