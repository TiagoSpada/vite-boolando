<script>
import FooterInformation from "./FooterInformation.vue";
import FooterSocial from "./FooterSocial.vue";
export default {
	name: "AppFooter",
	components: {
		FooterInformation,
		FooterSocial,
	},
};
</script>

<template>
	<footer>
		<div class="container">
			<div class="row">
				<FooterInformation />
				<FooterSocial />
			</div>
		</div>
	</footer>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/_variables" as *;
footer {
	background-color: $bg-color-footer;
	padding: 20px 0;
	color: #ffff;

	.row {
		justify-content: space-between;
	}
}
</style>
