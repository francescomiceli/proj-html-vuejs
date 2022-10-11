<!-- Menu Verticale 2 colonne nel footer -->

<template>
    <div>
        <div class="vertical-menu-title">{{ title }}</div>
        <ul>
            <li v-for="item in items" :key="item.id" class="vertical-menu-item"><a :href="item.url">{{ item.anchor
            }}</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'VerticalMenu',
    props: {
        title: String,
        items: Array,
    }
}
</script>

<style lang="scss" scoped>
.vertical-menu-title {
    font-size: 20px;
    margin-bottom: 20px;

}

.vertical-menu-item {
    margin-bottom: 7px;
}
</style>