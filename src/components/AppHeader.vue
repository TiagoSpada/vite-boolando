<script>
import AppLogo from "./AppLogo.vue";
import HeaderGender from "./HeaderGender.vue";
import HeaderIcon from "./HeaderIcon.vue";

export default {
	name: "AppHeader",
	components: {
		AppLogo,
		HeaderGender,
		HeaderIcon,
	},
};
</script>

<template>
	<header>
		<div class="container">
			<div class="row content-space-between">
				<HeaderGender class="col-33" />
				<AppLogo class="col-33" />
				<HeaderIcon class="col-33" />
			</div>
		</div>
	</header>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/_variables" as *;
header {
	background-color: $bg-color-header;
	padding: 20px 0;
}

.row {
	justify-content: space-between;
}
</style>
