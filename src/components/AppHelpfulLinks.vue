<template>
	<div class="help-links">
		<ul class="help-list">
			<li v-for="(help, index) in help" class="help-list-item">
				<div class="help-list-image-container">
					<img class="help-list-image" :src="help.img">
				</div>
				<div class="help-list-text">
					{{help.label}}
				</div>
			</li>
		</ul>
	</div>
</template>

<script>

	import toolDay from '../assets/img/super-tool-day.png'
	import location from '../assets/img/ic_location_b.png'
	import helpCenter from '../assets/img/ic_helpcenter.png'
	import plattUniversity from '../assets/img/ic_platt-u.png'

	export default {
		name: 'AppHelpfulLinks',
		data: function () {
			return {
				help: [
					{
						label: 'Super Tool Day & Dynamic Data Day',
						img: toolDay
					},
					{
						label: 'Branch Locations',
						img: location
					},
					{
						label: 'Help Center',
						img: helpCenter
					},
					{
						label: 'Platt University',
						img: plattUniversity
					},
				]
			}
		}
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';

	.help-links {
		margin-bottom: 20px;
	}
	.help-title {
		text-align:center;
		padding: 20px 0;
	}
	.help-list {
		display: flex;
		flex-wrap: wrap;
		flex-direction: row;
		justify-content: flex-end
	}

	.help-list-item {
		display: block;
		flex: 1 0 10%;
		text-align: center;
		background-color: white;
		margin-right: 50px;
		box-shadow: $box-shadow;
		padding: 20px 15px;
	}

	.help-list-item:last-child {
		margin-right: 0;

	}

	.help-list-text {
		padding: 6px;
		font-weight: 600;
	}

	.help-list-image-container {
		height: 80%;
	}

	@media screen and (max-width: $mobile-size) {
		.help-list-item {
			margin-right: 0px;
			flex: 1 0 40%;
		}
		.help-list-image-container {
			height: 70%;
		}
		.help-list-item:first-child {
			margin-right: 10px;
			margin-bottom: 10px;
		}
		.help-list-item:nth-child(2) {
			margin-left: 10px;
			margin-bottom: 10px;
		}
		.help-list-item:nth-child(3) {
			margin-right: 10px;
			margin-top: 10px;
		}
		.help-list-item:last-child {
			margin-left: 10px;
			margin-top: 10px;
		}
		.help-list-text {
			padding: 10px;
		}
	}
</style>
