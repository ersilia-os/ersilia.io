<template>
	<div class="ecosystem">

		<h5 class="text-center">Ersilia Ecosystem</h5>

		<div class="ecosystem__cols grid-cols grid-cols--4">

			<Card class="ecosystem__item" link="/docs">
				<icon-docs />
				<h4>Docs</h4>
				<p>Learn how to use the Ersilia toolbox.</p>
			</Card>

			<Card class="ecosystem__item" link="/plugins">
				<icon-plugins />
				<h4>Plugins</h4>
				<p>Enhance your Gridsome site with amazing plugins.</p>
			</Card>

			<Card class="ecosystem__item" link="/starters">
				<icon-starters />
				<h4>Starters</h4>
				<p>Browse A.I. models of biomedicine.</p>
			</Card>

			<Card class="ecosystem__item" link="/blog">
				<icon-blog />
				<h4>Blog</h4>
				<p>Articles from Ersilia team.</p>
			</Card>

		</div>
	</div>
</template>

<script>
import IconPlugins from '@/assets/images/icon-plugins.svg'
import IconDocs from '@/assets/images/icon-docs.svg'
import IconStarters from '@/assets/images/icon-starters.svg'
import IconBlog from '@/assets/images/icon-blog.svg'

export default {
	components: {
		IconPlugins,
		IconDocs,
		IconStarters,
		IconBlog
	}
}
</script>

<style lang="scss">
	.ecosystem {
		padding: calc(3% + 20px) 0 0;

		&__item {
			font-size: .9rem;

			svg {
				float: right;
				margin-top: -12px;
				margin-right: -10px;
			}
		}
	}
</style>
