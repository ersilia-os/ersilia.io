<template>
  <Section>
  	<h2 class="text-center mb-x2">Ersilia Sponsors</h2>
    <div class="grid-cols container container-md grid-cols--2">
    	<Card class="sponsor text-center">
	      <g-image src="~/assets/images/logo-netlify.svg" alt="Netlify"/>
	      <p>Thanks to <a href="https://fosshost.org"  rel="noopener" target="_blank">HossFost</a> for sponsoring Ersilia cloud infrastructure.</p>
    	</Card>
      <Card class="sponsor text-center">
	      <g-image src="~/assets/images/logo-algolia.svg" alt="Algolia"/>
	      <p>We are just getting started. Be the first one to sponsor us!</p>
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
