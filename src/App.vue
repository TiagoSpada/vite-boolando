<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import ProductList from "./components/ProductList.vue";
export default {
	name: "Boolando",
	components: {
		AppHeader,
		AppFooter,
		ProductList,
	},
};
</script>

<template>
	<AppHeader />
	<main>
		<ProductList />
	</main>
	<AppFooter />
</template>

<style scoped></style>
