<template>
	<div class="platt-plus">
		<div class="platt-plus-image-container">
			<img src="../assets/img/platt-plus.png">
		</div>
		<div class="platt-plus-get-started">
			<h5 class="platt-plus-text">Get Started Today</h5>
			<h5 class="platt-plus-text">Become a <span class="platt-plus-inner-text">Platt Plus</span> Member.</h5>
			<button class="platt-plus-button">Learn More</button>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'AppPlattPlus'
	}
</script>

<style lang="scss">
	@import '../styles/colors.scss';
	@import '../styles/common.scss';

	.platt-plus {
		background-color: white;
		padding: 30px 30px 40px;
		display:flex;
		align-items: center;
		margin-bottom: 20px;
		box-shadow: $box-shadow;

	}

	.platt-plus-text {
		font-weight: 600;
	}

	.platt-plus-inner-text {
		color: $primary-green;
	}

	.platt-plus-get-started {
		display:block;
		text-align:center;
		flex: 1.5;

	}

	.platt-plus-image-container {
		flex: 2;
	}

	.platt-plus-button {
		font-size: 16px;
		max-width: 230px;
		background-color: $light-gray;
		border-radius: 25px;
		padding: 12px 10px;
		border: none;
		outline: none;
		font-size: 14px;
		width: 100%;
		cursor: pointer;
		margin-top: 15px;
	}

	@media screen and (max-width: $mobile-size) {
		.platt-plus {
			flex-direction: column;
		}

		.platt-plus-image-container {
			margin-bottom: 20px;
		}
	}

</style>
