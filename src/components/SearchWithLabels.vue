<!-- Etichette nel Footer sotto input "Search" -->

<template>
    <div class="search-labels-wrapper">
        <div class="search-title">{{ title }}</div>
        <div class="labels-wrapper">
            <a v-for="item in items" :key="item.id" :href="item.url">{{ item.anchor }}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SearchWithLabels',
    props: {
        title: String,
        items: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

.search-labels-wrapper {

    .search-title {
        margin-bottom: 10px;
    }

    .labels-wrapper {
        margin: 0 -3px;

        a {
            font-size: 12px;
            display: inline-block;
            padding: 5px 13px;
            border: 1px solid #fff;
            border-radius: 30px;
            margin: 10px 3px 0;
            text-transform: uppercase;

            &:hover {
                color: #fff;
                background-color: $primary;
                border-color: $primary;
            }
        }
    }
}
</style>