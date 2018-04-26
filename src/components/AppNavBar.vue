<template>
	<div class="nav">
		<ul class="nav-items-container">
			<li v-for="(nav, index) in nav" :class="index === 0 ? 'nav-item-category' : 'nav-item'">
				<a>
					<img :class="nav.activeIcon ? 'desktop-only nav-item-image' : 'nav-item-image'" :src="nav.icon">
					<img v-if="nav.activeIcon" :src="nav.activeIcon" class="mobile-only nav-item-image">
					{{nav.label}}
				</a>
			</li>
		</ul>
	</div>
</template>

<script>
	import icCat from '../assets/ic/black/ic_categories.png'
	import icPlaylist from '../assets/ic/black/ic_playlist_add_check.png'
	import icList from '../assets/ic/black/ic_list.png'
	import icChatActive from '../assets/ic/green/ic_chat-active.png'
	import icChat from '../assets/ic/black/ic_chat.png'
	import icCheck from '../assets/ic/black/ic_check_circle.png'
	import icUser from '../assets/ic/black/ic_user_new.png'
	import icPlace from '../assets/ic/black/ic_place.png'

	export default {
		name: 'AppNavBar',
		data: function () {
			return {
				nav: [
					{
						label: 'Shop All Catergories',
						icon: icCat
					},
					{
						label: 'My Catalog',
						icon: icPlaylist
					},
					{
						label: 'My List',
						icon: icList
					},
					{
						label: 'Live Help',
						icon: icChat,
						activeIcon: icChatActive
					},
					{
						label: 'PIM',
						icon: icCheck
					},
					{
						label: 'Account',
						icon: icUser
					},
					{
						label: 'Branch Locations',
						icon: icPlace
					}
				]
			}
		}
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';
	@import '../styles/responsive.scss';

	.nav {
		background-color: white;
	}
	.nav-item-image {
		position: relative;
		right: 8px;
		width: 20px;
		vertical-align: middle;
	}

	.nav-items-container {
		display:flex;
		flex-wrap: wrap;
	}
	.nav-item-category {
		flex: 1 0 100%;
		display: flex;
		justify-content: center;
		padding: 15px;
		font-weight: 600;
	}
	.nav-item {
		display: flex;
		flex: 1 0 33%;
		border: solid 1px #ddd;
		padding: 12px 20px;
		justify-content: center;
	}

	@media screen and (max-width: $mobile-size) {
		.nav-item {
			flex: 100%;
			justify-content: left;
			background-image: url('../assets/ic/black/ic_arrow_forward.png');
			background-repeat: no-repeat;
			background-position: 98% center;
			background-origin: content-box;
			border-right: none;
			border-left: none;
		}
		.nav-items-container {
			padding: 5px 5px 0px 5px;
		}
		.nav-item-category {
			flex: 100%;
			padding: 20px 20px;
			font-size: 18px;
			justify-content: left;
			background-image: url('../assets/ic/black/ic_arrow_forward.png');
			background-repeat: no-repeat;
			background-position: 98% center;
			background-origin: content-box;
			border-right: none;
			border-left: none;
		}
	}
</style>
