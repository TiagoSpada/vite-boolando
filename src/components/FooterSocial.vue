<script>
export default {
	name: "FooterSocial",
};
</script>

<template>
	<div class="col">
		<div class="content">
			<h4>Trovaci anche su</h4>
			<ul>
				<li><i class="fab fa-twitter-square"></i></li>
				<li><i class="fab fa-facebook-square"></i></li>
				<li><i class="fab fa-instagram-square"></i></li>
				<li><i class="fab fa-pinterest-square"></i></li>
				<li><i class="fab fa-youtube-square"></i></li>
			</ul>
		</div>
	</div>
</template>

<style scoped lang="scss">
.content {
	margin: auto 14px;
	h4 {
		margin-bottom: 5px;
	}
	ul {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		li {
			i {
				font-size: 22px;
				cursor: pointer;
			}
		}
	}
}
</style>
