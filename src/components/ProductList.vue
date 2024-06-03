<script>
import productsJson from "./db.json";
import ProductElement from "./ProductElement.vue";
export default {
	name: "ProductList",
	components: {
		ProductElement,
	},
	data() {
		return {
			products: productsJson.products,
			ProvaD: true,
		};
	},
	methods: {
		OriginalPrice(DiscountedPrice, Discount) {
			if (Discount.type === "tag") return;
			// console.log(Discount);
			const OriginalPirce =
				(DiscountedPrice * 100) / (100 - parseFloat(Discount.value.slice(1)));
			return parseFloat(OriginalPirce).toFixed(2);
		},
	},
};
</script>
<template>
	<section>
		<div class="container">
			<div class="row">
				<!-- ripeto l'elemento in base la numero di elementi e passo i valori che mi servono -->
				<ProductElement
					v-for="(product, index) in products"
					:frontImage="product.frontImage"
					:backImage="product.backImage"
					:brand="product.brand"
					:name="product.name"
					:price="product.price"
					:badges="product.badges"
					:OriginalPrice="
						OriginalPrice(
							product.price,
							product.badges[product.badges.length - 1]
						)
					"
				/>
			</div>
		</div>
	</section>
</template>

<style scoped lang="scss">
section {
	padding: 50px 0;
	.row {
		.product {
			width: calc(100% / 3 - 20px);
			margin: 10px;
		}
	}
}
</style>
