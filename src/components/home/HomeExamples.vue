<template>
	<Section dots="true">
		<h2 class="container text-center">
      Meet our team
    </h2>
    <p class="lead text-center container-md">
    	We are always excited to hear about projects, ideas or possible collaborations.
    </p>

		<div class="home-examples mb-x2">
			<Examples />
		</div>

    <p class="home-links text-center ">
      <g-link  to="//ersilia.io" class="button primary button--large">
        Contact us!
      </g-link>
    </p>
	</Section>
</template>

<script>
import Examples from '~/components/Examples.vue'
export default {
	components: {
		Examples
	}
}
</script>

<style>
.home-examples {
	margin: 0 auto;
	max-width: 960px;
}
</style>
