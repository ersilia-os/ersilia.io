<template>
  <Section dots="true">
		<h2 class="text-center mb-x2">Our team</h2>
    <div class="homepage-features grid-cols">

      <Feature>
				<g-image src="~/assets/images/ersilia-team-03.png" width="200" blur="0" retina="true" alt="Edoardo Gaude" />
        <h3>Edoardo Gaude</h3>
        <p>CEO and Trustee
        </p>
      </Feature>

      <Feature>
				<g-image src="~/assets/images/ersilia-team-02.png" width="200" blur="0" retina="true" alt="Miquel Duran" />
        <h3>Miquel Duran</h3>
        <p>CSO and Trustee
        </p>
      </Feature>

      <Feature>
				<g-image src="~/assets/images/ersilia-team-01.png" width="200" blur="0" retina="true" alt="Gemma Turon" />
        <h3>Gemma Turon</h3>
         <p>Project Manager
          </p>
      </Feature>

    </div>

  </Section>
</template>

<script>
import VueLogo from '~/assets/images/vue-logo.svg'
import GraphQlLogo from '~/assets/images/graphql-logo.svg'
export default {
  props: ['icon'],
  components: {
    VueLogo,
    GraphQlLogo,
  },
  computed: {
    iconClasses() {
      let classes = []
      return classes
    }
  }
}
</script>
