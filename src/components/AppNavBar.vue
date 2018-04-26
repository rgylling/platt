<template>
    <div class="nav">
        <ul class="nav-items-container">
            <li class="nav-item-category">
                <a>Shop all catergories</a>
            </li>
			<li class="nav-item">
				<a>My Catalog</a>
			</li>
			<li class="nav-item">
				<a>My List</a>
			</li>
			<li class="nav-item">
				<a>Live Help</a>
			</li>
			<li class="nav-item">
				<a>PIM</a>
			</li>
			<li class="nav-item">
				<a>Account</a>
			</li>
			<li class="nav-item">
				<a>Branch Locations</a>
			</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'AppNavBar'
}
</script>

<style lang="scss">

	.nav-items-container {
		display:flex;
		flex-wrap: wrap;
	}
	.nav-item-category {
		flex: 1 0 100%;
		display: flex;
		justify-content: center;
	}
	.nav-item {
		flex: 1 0 33%;
	}
</style>
