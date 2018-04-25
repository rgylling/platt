<template>
    <div class="header">
        <div class="header-inner">
        <img src="../assets/img/logo.png"
        alt="Platt Electric Logo"
        />
            <ul class="actions">
                <li>
                    <img src="../assets/ic/white/ic_search.png" />
                </li>
                <li>
                    <img src="../assets/ic/white/ic_shopping_cart.png" />

                </li>
                <li>
                    <img src="../assets/ic/white/ic_person.png" />
                </li>
                <li>
                    <img src="../assets/ic/white/ic_menu.png" />
                </li>
            </ul>
        </div>
        <div class="search-container">
            <input class="search"
            type="text"
            placeholder="What are you looking for?"
            />
        </div>
    </div>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style lang="scss">
    .header {
        background-color: #008838;
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
    }
    .search-container {
        padding: 10px 3px 5px;
    }
    .search {
        width: 100%;
        font-size: 16px;
        padding: 15px;
        border-radius: 3px;
        background-image: url('../assets/ic/black/ic_search.png');
        background-repeat: no-repeat;
        background-position: right center;
        background-origin: content-box;
        outline: none;
    }
</style>
