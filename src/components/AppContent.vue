<template>
    <div class="content">
		<AppProducts></AppProducts>
		<AppDeals></AppDeals>
		<AppRecentlyViewed></AppRecentlyViewed>
		<AppHelpfulLinks></AppHelpfulLinks>
		<AppMobile></AppMobile>

    </div>
</template>

<script>

import AppProducts from './AppProducts'
import AppDeals from './AppDeals'
import AppRecentlyViewed from './AppRecentlyViewed'
import AppHelpfulLinks from './AppHelpfulLinks'
import AppMobile from './AppMobile'

export default {
  name: 'AppContent',
  components: {
	  AppProducts,
	  AppDeals,
	  AppRecentlyViewed,
	  AppHelpfulLinks,
	  AppMobile
  }
}
</script>

<style lang="scss">

.content {
	background-color:#ddd;
}

</style>
