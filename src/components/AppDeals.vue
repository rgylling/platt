<template>
	<img class="deals-image desktop-only" src="../assets/panel/deal.png">
</template>

<script>
	export default {
		name: 'AppDeals'
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';

	.deals-image {
		width: calc(50% - 10px);
		box-shadow: $box-shadow;
	}

</style>
