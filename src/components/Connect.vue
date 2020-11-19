<template>
  <div class="connect">

    <transition-group name="fade">
      <div class="connect__slide" key=1 v-show="activeSlide == 0"><g-image class="connect__logos" src="~/assets/images/diagram-02.png" width="1180" blur="10" retina="true" alt="The Modern Web Logos" /></div>
      <div class="connect__slide" key=2 v-show="activeSlide == 1"><g-image class="connect__logos" src="~/assets/images/diagram-03.png" width="1180" blur="10" retina="true" alt="The Modern Web Logos 2" /></div>
      <div class="connect__slide" key=3 v-show="activeSlide == 2"><g-image class="connect__logos" src="~/assets/images/diagram-04.png" width="1180" blur="10" retina="true" alt="The Modern Web Logos 3" /></div>
    </transition-group>

    <g-image class="connect__main" src="~/assets/images/diagram-05.png" width="1180" blur="10" retina="true" alt="The Modern Web Background" />

    <svg class="connect__dots" width="958" height="833" viewBox="0 0 958 833" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M378.49,171.57c14,.81,23.31,12.08,29.76,22.39,14,22.46,25.3,47.16,23.18,72.36-.77,9.23-3,19.58,4,26.82" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
      <path d="M240.2,390c11.32-3.09,23,2.65,33.18,8.47,46.89,26.81,92.49,59.86,145.88,68" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
      <path d="M293.56,604.13c-1.61-12.85-3.21-26-.7-38.66s9.88-25.16,21.72-30.41" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
      <path d="M574.48,619.67c-13.63-2.13-23.44-15.66-24.76-29.4S554,563,561.52,551.43s17-21.74,24.79-33.13c8-11.62,14.29-25.76,11.14-39.48" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
      <path d="M721.46,364.82c-18-1.08-36.2-2.16-54.05.54a83.39,83.39,0,0,0-16.92,4.18c-8.7,3.28-16.52,8.47-24.79,12.73a125.77,125.77,0,0,1-33.1,11.55C584,395.53,574,396,567.42,390.06" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
      <path d="M666.78,205.19c1.77,14.43,3.51,29.27-.14,43.34-5,19.35-19.49,34.6-33.42,48.94" stroke="#2AD6A1" stroke-width="8" stroke-linecap="round" stroke-linejoin="round" stroke-dasharray="1 30"/>
    </svg>

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
