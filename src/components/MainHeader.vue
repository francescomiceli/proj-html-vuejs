<!-- Main Header -->

<template>
    <header id="main-header">
        <nav class="d-flex justify-content-between align-items-center">
            <div>
                <!-- Importazione componente Logo -->
                <BaseLogo />
            </div>
            <div class="d-flex align-items-center">
                
                <!-- collegamento a App.vue e agli elementi della navigazione tramite props-array -->
                <RowMenu :items="mainMenuItems" />. 
                <a class="btn-primary" id="header-button" href="#">VIEW COURSES</a>
            </div>
        </nav>
    </header>
</template>

<script>
// Importazione componenti Logo e Navigazione Header

import BaseLogo from './BaseLogo.vue';
import RowMenu from './RowMenu.vue';


// Esportazione  "Main Header" - i componenti logo e navigazione, questo collegato tramite le props all'array 
export default {
    name: "MainHeader",
    components: { BaseLogo, RowMenu },
    props: {
        mainMenuItems: Array,
    }
}
</script>

<style lang="scss" scoped>
#main-header {
    font-size: 17px;
    position: absolute;
    top: 60px;
    left: 60px;
    right: 60px;
    z-index: 10;

    #header-button {
        margin-left: 45px;
        padding: 20px 40px;
        border-radius: 50px;
    }
}
</style>