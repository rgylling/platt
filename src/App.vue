<template>
	<div id="app">
		<AppHeader></AppHeader>
		<AppNavBar></AppNavBar>
		<AppContent></AppContent>
		<AppFooter></AppFooter>

	</div>
</template>

<script>
import AppHeader from './components/AppHeader'
import AppNavBar from './components/AppNavBar'
import AppContent from './components/AppContent'
import AppFooter from './components/AppFooter'

export default {
	name: 'app',
	components: {
		AppHeader,
		AppNavBar,
		AppContent,
		AppFooter
	}
}
</script>

<style lang="scss">
	@import './styles/reset.scss';
	@import './styles/type.scss';
	@import './styles/colors.scss';
	@import './styles/base.scss';


	#app {
		max-width: 1025px;
		margin: 0 auto;
	}

</style>
