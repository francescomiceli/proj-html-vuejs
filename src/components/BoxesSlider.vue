<!-- Slider sezione -->

<template>
    <div>
        <ul class="thumbs-container d-flex justify-content-center">
            <li v-for="item in items" :key="item.id"
                class="box c-pointer d-flex justify-content-center align-items-center"
                :class="{ 'clicked': currentActiveIndex === item.id }" @click="currentActiveIndex = item.id">
                <figure class="box-content">
                    <img :src="require(`../assets/img/${item.icon}`)" :alt="item.title">
                    <figcaption>{{ item.title }}</figcaption>
                </figure>
            </li>
        </ul>

        <ul class="slider-container">
            <li v-for="item in items" :key="item.id" class="slider-content"
                :class="{ 'd-block': currentActiveIndex === item.id }">
                <div class="row">
                    <div class="col-6">
                        <img :src="require(`../assets/img/${item.img}`)" :alt="item.title">
                    </div>
                    <div class="slider-right col-6">
                        <h4>{{ item.title }}</h4>
                        <p class="slider-text">{{ item.text }}</p>
                        <MainButton anchor="Read More" :url="item.url" scheme="danger" />
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
import MainButton from './MainButton.vue';
export default {
    name: "BoxesSlider",
    props: {
        items: Array,
    },
    data() {
        return {
            currentActiveIndex: 1,
        }
    },
    components: { MainButton },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

figure {
    margin-bottom: 0;
}

.thumbs-container {
    box-shadow: 0 0 20px 1px #F0F0F0;

    .box {
        font-family: 'Roboto', sans-serif;
        color: $danger;
        width: 230px;
        height: 200px;
        border: 1px solid #F0F0F0;
        position: relative;

        img {
            height: 80px;
            margin-bottom: 15px;
        }

        &.clicked {
            color: #fff;
            background-color: $danger;

            img {
                filter: brightness(0) invert(1);
            }

            &::after {
                content: "";
                border-top: 15px solid $danger;
                border-right: 15px solid transparent;
                border-bottom: 15px solid transparent;
                border-left: 15px solid transparent;
                position: absolute;
                bottom: calc(0% - 30px);
                left: 50%;
                transform: translateX(-50%);
            }
        }
    }
}


.slider-container {
    padding: 100px 0;

    .slider-content {
        display: none;
        margin: 0 auto;
        max-width: 1100px;

        .slider-right {
            text-align: start;
        }

        .slider-text {
            padding: 30px 0;
            color: $light;
        }
    }
}
</style>