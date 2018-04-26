<template>
	<div class="footer">
		<div class="footer-inner">
			<div class="footer-top">
				<h4 class="font-bold">Support Center</h4>
				<div class="footer-number">
					<h4 class="font-bold">800-25-Platt</h4>
					<h6 class="font-bold">800-257-5288</h6>
				</div>
			</div>
			<div class="footer-bottom">
				<h5 class="font-bold">4 a.m. - 12 a.m. (pst)</h5>
				<h5 class="font-bold">7 Days a week</h5>
			</div>
			<button class="live-help-button">Live Help</button>
		</div>
		<ul class="footer-nav">
			<li class="font-bold">Contact Us</li>
			<li class="font-bold">What's New</li>
			<li class="font-bold">FAQ's</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'AppFooter'
	}
</script>

<style lang="scss">
	@import '../styles/colors.scss';

	.live-help-button {
		background-color: $light-gray;
		padding: 14px;
		border-radius: 25px;
		border: none;
		outline: none;
		font-size: 16px;
		width: 100%;
		cursor: pointer;
		max-width: 230px;
		background-image: url('../assets/ic/black/ic_comment.png');
		background-repeat: no-repeat;
		background-position: 20% center;
		background-origin: content-box;
	}

	.footer {
		background-color: $dark-gray;
		padding-bottom: 30px;
		margin-bottom: 20px;
	}
	.footer-inner {
		text-align: center;
		padding: 30px 15px;
	}
	.footer-top {
		color: $light-gray-text;
	}
	.footer-bottom {
		color: $dark-gray-text;
		margin-bottom: 35px;
	}
	.footer-nav {
		display: flex;
		justify-content: space-around;
		color: $light-gray;
	}
	.footer-number {
		margin-bottom: 12px;
	}
	.font-bold {
		font-weight: 600;
	}
</style>
