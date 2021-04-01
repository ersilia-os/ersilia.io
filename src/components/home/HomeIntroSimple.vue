<template>
  <Section class="intro" dots="false">
    <div class="container text-center ">

        <h1 class="intro__title">
          <span>Welcome to the Ersilia Model Hub!</span>
        </h1>

        <p class="intro__lead lead post mb">
          Open Source Drug Discovery for Global Health
        </p>
        </p>
        <p class="intro__links">
          <g-link  to="/soon/" class="button primary button--large">
            <span>Check our Models</span>
          </g-link>
        </p>

        <p class="intro__info">
          <span>MIT Licensed. </span>
          <a href="//github.com/ersilia-os/ersilia" target="_blank" rel="noopener noreferrer">
            <span>GitHub</span>
          </a>
        </p>
    </div>
  </Section>
</template>

<static-query>
query {
  metadata {
    gridsomeVersion
  }
}
</static-query>

<style lang="scss">
.intro {
  padding: calc(2% + var(--space)) 0;

  &__title {
    font-size: 3rem;
    font-weight: 600;
    margin-left: auto;
    margin-right: auto;
    letter-spacing: -1px;
    margin-bottom: 0;

    @media screen and (max-width: 850px) {
      & {
        font-size: 2rem;
      }
    }
  }

  &__lead {
    max-width: 650px;
    margin-left: auto;
    margin-right: auto;
    font-size: 1.3rem;
    @media screen and (max-width: 850px) {
      & {
        font-size: 1rem;
      }
    }
  }

  &__info {
    font-size: .9rem;
    margin-top: -1rem;
  }

  &__keywords {
    position: relative;
    display: block;
  }
}
</style>
