<template>
	<div class="recently-viewed">
		<div class="recently-viewed-header">
			<p class="header-left">Recently viewed</p>
			<p class="pull-right view-all">View all</p>
		</div>
		<div class="recently-viewed-items">
			<div class="item-container">
				<img src="../assets/recent/11.png">
			</div>
			<div class="item-container">
				<img src="../assets/recent/22.png">
			</div>
			<div class="item-container">
				<img src="../assets/recent/22.png">
			</div>
		</div>

	</div>
</template>

<script>
	export default {
		name: 'AppRecentlyViewed'
	}
</script>

<style lang="scss">
	@import '../styles/colors.scss';
	@import '../styles/common.scss';

	.recently-viewed {
		background-color: white;
		padding: 10px 15px;
		width: calc(50% - 10px);
		box-shadow: $box-shadow;
	}

	.recently-viewed-header {
		margin-bottom: 20px;
	}

	.header-left {
		display: inline;
		font-weight: 600;
	}

	.pull-right {
		float: right;
	}

	.recently-viewed-items {

	}

	.item-container {
		width: 30%;
		text-align: center;
		display: inline-block;
	}

	.view-all {
		color: $primary-green;
		font-weight: 600;
	}

	@media screen and (max-width: $mobile-size) {
		.recently-viewed {
			width: 100%;
		}
	}

</style>
