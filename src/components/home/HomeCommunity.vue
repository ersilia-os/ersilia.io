<template>
  <Section>
  	<h2 class="text-center mb-x2">Partners</h2>
    <div class="grid-cols container container-md grid-cols--2">
      <Card class="sponsor text-center">
        <g-link to="https://fosshost.org">
          <g-image src="~/assets/images/Fosshost-logo-green.svg" alt="FossHost"/>
        </g-link>
        <p>Thanks to <a href="https://fosshost.org"  rel="noopener" target="_blank">FossHost</a>
           for providing world-class hosting and supporting the growth, advancement
           and adoption of free software.
        </p>
    	</Card>
      <Card class="sponsor text-center">
        <g-link to="https://fosshost.org">
          <g-image src="~/assets/images/PDD-UpdatedLogo-1.png" alt="PDD"/>
        </g-link>
        <p>We endorse the <a href="https://digitalprinciples.org/"  rel="noopener" target="_blank">Principles for Digital Development</a>.
        </p>
    	</Card>
    </div>
  </Section>
</template>

<style lang="scss">
.sponsor {
	img {
		max-height: 35px;
		width: auto;
	}
}
</style>
