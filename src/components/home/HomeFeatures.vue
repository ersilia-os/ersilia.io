<template>
  <Section dots="true">
    <div class="homepage-features grid-cols">

      <Feature>
        <h3>Data driven</h3>
        <p>Ersilia technology is based on <strong>experimental data</strong> and achieves state-of-the-art performance through the integration of chemical, genomic and biomedical text records.
        </p>
      </Feature>

      <Feature>
        <h3>Free for everyone</h3>
        <p>Our resource is and will always be open source. We truly believe in open source science as a means to generate <strong>low revenue drugs</strong> and thus contribute to a more egalitarian world.
        </p>
      </Feature>

      <Feature>
        <h3>Closer to the clinics</h3>
         <p>Unlike conventional methods, Ersilia capitalizes on <strong>bioactivity signatures</strong> that embed the characteristics of small molecules, including their targets and side-effects profiles.
          </p>
      </Feature>

      <Feature>
        <h3>Democratized technology</h3>
        <p>We put significant effort on making A.I. models accessible to the broad scientific community, not only to data scientists and I.T. engineers.</p>
      </Feature>

      <Feature>
        <h3>Neglected diseases</h3>
        <p>Our primary interest is the development of therapies for diseases of the <strong>low and middle income countries</strong>.
        </p>
      </Feature>

      <Feature>
        <h3>Unique expertise</h3>
        <p>Our team merges expertise in chemistry, molecular biology and computational pharmacology with a natural enthusiasm for global health.</p>
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
