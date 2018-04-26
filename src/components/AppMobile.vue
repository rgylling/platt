<template>
	<div class="mobile">
		<div class="mobile-image">
		</div>
		<div class="mobile-text-container">
			<h6 class="mobile-text">Shop better, download the Platt App today</h6>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'AppMobile'
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';

	.mobile {
		background-color: white;
		box-shadow: $box-shadow;
		text-align: center;
		margin-bottom: 20px;
	}

	.mobile-image {
		min-height: 150px;
		width: 100%;
		background-image: url('../assets/panel/app-get-banner.png');
		background-repeat: no-repeat;
		background-size: cover;
	}

	.mobile-text-container {
		padding: 10px;
	}

	.mobile-text {
		margin: 0;
		font-weight: 600;
	}

	@media screen and (max-width: $mobile-size) {
		.mobile-image {
				background-position: right center;
		}
	}

</style>
