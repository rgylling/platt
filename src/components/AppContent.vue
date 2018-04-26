<template>
	<div class="content">
		<AppProducts></AppProducts>
		<AppDealsMobile></AppDealsMobile>
		<AppPlattPlus></AppPlattPlus>
		<div class="content-deals">
			<AppDeals></AppDeals>
			<AppRecentlyViewed></AppRecentlyViewed>
		</div>
		<AppHelpfulLinks></AppHelpfulLinks>
		<AppMobile></AppMobile>
	</div>
</template>

<script>

	import AppProducts from './AppProducts'
	import AppDealsMobile from './AppDealsMobile'
	import AppPlattPlus from './AppPlattPlus'
	import AppDeals from './AppDeals'
	import AppRecentlyViewed from './AppRecentlyViewed'
	import AppHelpfulLinks from './AppHelpfulLinks'
	import AppMobile from './AppMobile'

	export default {
		name: 'AppContent',
		components: {
			AppProducts,
			AppDealsMobile,
			AppPlattPlus,
			AppDeals,
			AppRecentlyViewed,
			AppHelpfulLinks,
			AppMobile
		}
	}
</script>

<style lang="scss">
	@import '../styles/colors.scss';
	@import '../styles/common.scss';

	.content {
		background-color: $light-gray;
		padding: 0 15px 5px;
	}

	.content-deals {
		display: flex;
		justify-content: space-between;
		margin-bottom: 20px;
	}

	@media screen and (max-width: $mobile-size) {
		.content {
			padding: 0 10px 5px;
		}
	}

</style>
