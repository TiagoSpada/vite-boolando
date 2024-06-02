<script>
export default {
	name: "HeaderIcon",
};
</script>
<template>
	<div>
		<ul>
			<li>
				<a href=""><i class="fas fa-user"></i></a>
			</li>
			<li>
				<a href=""><i class="fas fa-heart"></i> </a>
			</li>
			<li>
				<a href=""><i class="fas fa-bag-shopping"></i></a>
			</li>
		</ul>
	</div>
</template>

<style scoped lang="scss">
div {
	margin: auto 0;

	ul {
		display: flex;
		flex-wrap: wrap;
		flex-direction: row-reverse;
	}

	li {
		margin: 0 14px;
	}

	a {
		color: #ffff;
		font-family: Arial, Helvetica, sans-serif;
		font-size: 14px;
		font-weight: 600;
	}
}
</style>
