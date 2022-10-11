<!-- Footer -->

<template>
    <footer id="footer">
        <nav class="container">
            <div class="row">
                <div class="col-4">
                    <BaseLogo />
                    <p class="footer-text">EduPrime is the most versatile WordPress theme for educational purposes,
                        showcasing
                        universities, courses, secondary schools etc.
                    </p>
                    <SocialLabels />
                </div>
                <div class="col-4">
                    <div class="row">
                        <div class="col">
                            <!-- Collegamento tramite le props all'array "getEduMenuItems" -->
                            <VerticalMenu title="GetEduPrime" :items="getEduMenuItems" />
                        </div>
                        <div class="col">
                            <VerticalMenu title="Networking" :items="NetworkingMenuItems" />
                        </div>
                    </div>
                </div>
                <div class="col-4 text-end">
                    <BaseInput class="mb-4" placeholder="Search..." icon="fa-magnifying-glass" />
                    <SearchWithLabels title="Search categories" :items="CategoriesLabels" class="mb-3" />
                    <div class="text-primary">ModelTheme. All rights reserved.</div>
                </div>
            </div>
        </nav>
    </footer>
</template>

<script>
import BaseLogo from './BaseLogo.vue';
import SocialLabels from './SocialLabels.vue';
import VerticalMenu from './VerticalMenu.vue';
import BaseInput from './BaseInput.vue';
import SearchWithLabels from './SearchWithLabels.vue';
export default {
    name: "MainFooter",
    components: { BaseLogo, SocialLabels, VerticalMenu, BaseInput, SearchWithLabels },
    props: {
        CategoriesLabels: Array,
        getEduMenuItems: Array,
        NetworkingMenuItems: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

#footer {
    color: #fff;
    padding: 100px 0 80px;
    background-color: $danger;

    .footer-text {
        padding: 30px 0 15px;
    }
}
</style>