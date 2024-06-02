<script>
export default {
	name: "GenderLink",
};
</script>
<template>
	<div>
		<ul>
			<li><a href="">Donna</a></li>
			<li><a href="">Uomo</a></li>
			<li><a href="">Bambini</a></li>
		</ul>
	</div>
</template>
<style scoped lang="scss">
div {
	margin: auto 0;

	ul {
		display: flex;
		flex-wrap: wrap;
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
