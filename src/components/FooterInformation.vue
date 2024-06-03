<script>
export default {
	name: "FooterInformation",
};
</script>

<template>
	<div class="col">
		<div class="content">
			<h3>Boolando s.r.l</h3>
			<ul>
				<li>Informazioni Legali</li>
				<li>Informativa sulla privacy</li>
				<li>Diritto di recesso</li>
			</ul>
		</div>
	</div>
</template>

<style scoped lang="scss">
.content {
	margin: auto 14px;
	h3 {
		margin-bottom: 10px;
	}
	ul {
		display: flex;
		flex-wrap: wrap;
		gap: 10px;
		font-size: 12px;
	}
}
</style>
