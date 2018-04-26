<template>
	<div class="header">
		<div class="header-inner">
			<img src="../assets/img/logo.png"
			alt="Platt Electric Logo"
			/>
			<ul class="actions">
				<li class="action-button">
					<img src="../assets/ic/white/ic_search_icon.png" />
				</li>
				<li class="action-button">
					<img src="../assets/ic/white/ic_shopping_cart.png" />
				</li>
				<li class="action-button">
					<img src="../assets/ic/white/ic_person.png" />
					<span class="notification"></span>
				</li>
				<li class="action-button">
					<img src="../assets/ic/white/ic_menu.png" />
				</li>
			</ul>
		</div>
		<AppSearch></AppSearch>
	</div>
</template>

<script>
	import AppSearch from './AppSearch'

	export default {
		name: 'AppHeader',
		components: {
			AppSearch
		}
	}
</script>

<style lang="scss">
	@import '../styles/colors.scss';

	.header {
		background-color: $header-green;
		padding: 10px;
	}
	.header-inner {
		display: flex;
		align-items: center;
	}
	.actions {
		display: flex;
		margin-left: auto;
		align-items: center;
		position: relative;
	}

	.notification {
		position: absolute;
		width: 5px;
		height: 5px;
		background-color: #ffbf00;
		border-radius: 100%;
		top: -3px;
		right: 42px;
		box-shadow: 0 1px 2px 1px rgba(0, 0, 0, 0.35);
	}

	.action-button {
		margin: 0 10px;
	}
</style>
