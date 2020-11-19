<template>
  <Section class="works">
    <div class="grid-cols grid-cols--gap-large grid-cols--full-md">

      <Card title="Research">
        <h4>Scientific literature</h4>
        <p>We gather information from papers related to drug discovery</p>
        <h4>Large scale datasets</h4>
        <p>We integrate the major public repositories of small molecules</p>
        <h4>A.I. algorithms</h4>
        <p>We incorporate the latest advances in artificial intelligence</p>

        <template slot="outer">
          <Dots class="hide-for-small"/>
          <Dots class="dots--vertical show-for-small"/>
        </template>
      </Card>

      <Card title="Machine learning" class="text-center flex-align-middle">

        <div class="works__logo">
          <gridsome-logo />
          <div class="works__pulse-bg"></div>
          <div class="works__pulse-bg"></div>
        </div>

        <p class="works__powered-by">
          Powered by the <br/><strong>Chemical Checker</strong>
        </p>

        <ul class="works__tools flex gap-15 text-center flex--center">
          <li><g-link to="//bioactivitysignatures.org">Bioactivity signatures</g-link></li>
        </ul>

        <template slot="outer">
          <Dots class="hide-for-small"/>
          <Dots class="dots--vertical show-for-small"/>
        </template>
      </Card>

      <Card title="Predict">
        <h4>Deployed A.I. models</h4>
        <p>
          Our computational models are ready to be used. No need for expertise.
        </p>

        <ul class="bullet-list mb">
          <li><Bullet /><g-link to="/docs/">Single web app predictions</g-link></li>
          <li><Bullet /><g-link to="/docs/">Batch predictions through API</g-link></li>
          <li><Bullet /><g-link to="/docs/">Download and run locally</g-link></li>
          <li><Bullet /><g-link to="/docs/">Orchestrate multiple models</g-link></li>
        </ul>
      </Card>

    </div>
  </Section>
</template>

<script>
import GraphQlLogo from '~/assets/images/graphql-logo.svg'
import VueLogo from '~/assets/images/vue-logo.svg'
import WebpackLogo from '~/assets/images/webpack-logo.svg'
import GridsomeLogo from '~/assets/images/gridsome-small-white.svg'
import Bullet from '~/assets/images/bullet.svg'
import Dots from '~/components/Dots.vue'

export default {
  components: {
    Bullet,
    VueLogo,
    GridsomeLogo,
    WebpackLogo,
    GraphQlLogo,
    Dots
  }
}
</script>

<style lang="scss">
.works {

  .bullet-list li {
    margin-bottom: .3rem;
  }

  .card__inner {
    padding: 30px 40px;
  }

  @media screen and (max-width: 850px) {
    .card {
      margin-bottom: 40px;
    }
  }


  &__tools {
    font-weight: 500;
    border: 1px solid var(--border-color);
    max-width: 230px;
    border-radius: 4px;
    z-index: 9;
    margin: 0 auto!important;
    padding: 10px;

    li {
      margin-bottom: 0;
    }
  }

  &__logo {
    background-color: var(--primary-color);
    width: 100px;
    z-index: 1;
    position: relative;
    height: 100px;
    margin: 0 auto;
    margin-top: 18%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    border-radius: 100%;
    z-index: 0;
    margin-bottom: 1rem;
    animation: bounce 2s infinite;

    svg {
      width: 70px;
      height: 70px;
    }
  }

  &__pulse-bg {
    animation: pulse 2s infinite;
    border: 3px solid var(--primary-color);
    width: 100px;
    height: 100px;
    position: absolute;
    border-radius: 100%;
    opacity: .3;
    z-index: -1;

    + .works__pulse-bg {
      width: 95px;
      height: 95px;
      animation-delay: .3s;
    }
  }

  &__powered-by {
    opacity: .8;
    line-height: 1.3;
    padding-bottom: 1.2rem;
  }
}
</style>
