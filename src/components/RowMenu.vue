
<!-- MENU ORIZZONTALE HEADER -->
<template>
    <ul class="d-flex">
        <li v-for="item in items" :key="item.id">
            <a :href="item.link">
                <span>{{ item.anchor }}</span>
                
            </a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'RowMenu',
    props: {
        items: Array,
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

ul {
    li {
        margin-left: 35px;

        a {

            &.active {
                color: $primary;
            }

            span {
                vertical-align: middle;
            }

            .fa-caret-down {
                font-size: 10px;
                padding-left: 10px;
                vertical-align: middle;
            }
        }
    }
}
</style>



