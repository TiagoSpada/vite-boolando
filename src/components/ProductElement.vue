<script>
export default {
	name: "ProductElement",
	props: [
		"frontImage",
		"backImage",
		"brand",
		"name",
		"price",
		"badges",
		"OriginalPrice",
	],
	data() {
		return {
			MouseHover: false,
		};
	},
	methods: {
		DiscountorTag(type) {
			if (type === "discount") return "discount-label";
			else if (type === "tag") return "tag-label";
		},
	},
};
</script>
<template>
	<div class="product">
		<!-- IMMAGINE PRODOTTO (con gestione del mousehover)-->
		<div
			class="immagine"
			@mouseover="MouseHover = true"
			@mouseleave="MouseHover = false"
		>
			<!-- IMMAGINE VISUALIZZATA ALL'APERTURA DELLA PAGINA -->
			<img
				:src="`/img/${frontImage}`"
				:alt="name"
				:class="{ active: !MouseHover }"
			/>
			<!-- IMMAGINE VISUALLITA CON L'HOVER DEL MOUSE -->
			<img
				:src="`/img/${backImage}`"
				:alt="name"
				:class="{ active: MouseHover }"
			/>
			<!-- BADGE DEL PRODOTTO -->
			<div class="label-product">
				<!-- PASSO L'ARRAY DEI BADGE E IN BASE AL TIPO ASSOCIO ALLO SPAN UNA CLASSE -->
				<span
					v-for="(badge, i) in badges.slice().reverse()"
					:class="DiscountorTag(badge.type)"
					>{{ badge.value }}</span
				>
			</div>
			<!-- CUORE DELLA WISH LIST -->
			<div class="wishlist"><i class="fas fa-heart"></i></div>
		</div>
		<!-- INFORMAZIONE DEL PRODOTTO -->
		<div class="information-product">
			<small class="brand">{{ brand }}</small>
			<div class="product-type">{{ name.toUpperCase() }}</div>
			<div class="price">
				{{ price }} &euro;
				<!-- FUNZIONE CHE VERIFICA E SE IL PRODOTTO E' SCONTATO E NE CALCOLA IL PREZZO ORIGINALE (da vedere nel file ProductList.vue) -->
				<span class="discount" v-show="OriginalPrice"
					>{{ OriginalPrice }}&euro;
				</span>
			</div>
		</div>
	</div>
</template>
<style scoped lang="scss">
.immagine {
	position: relative;

	img {
		max-width: 100%;
		display: none;
	}
	.active {
		display: block;
	}
	.label-product {
		position: absolute;
		color: white;
		bottom: 45px;
		font-size: 14px;
		span {
			padding: 5px 8px;
		}
		.discount-label {
			background-color: #ff0000;
			margin-right: 5px;
		}
		.tag-label {
			background-color: #008000;
		}
	}

	.wishlist {
		position: absolute;
		z-index: 999;
		top: 1%;
		right: 0;
		background-color: white;
		font-size: 30px;
		width: 50px;
		height: 50px;
		text-align: center;
		align-content: center;
		cursor: pointer;
	}
	.wishlist:hover {
		color: red;
	}
}
.information-product {
	margin-bottom: 20px;
	.product-type {
		font-size: 16px;
		font-weight: 560;
	}

	.price {
		font-size: 13px;
		color: red;
		font-weight: 800;
	}

	.discount {
		color: black;
		font-weight: normal;
		text-decoration: line-through;
	}
}
</style>
