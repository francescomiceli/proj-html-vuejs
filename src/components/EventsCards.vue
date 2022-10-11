<!-- Sezione Upcoming Events -->

<template>
    <div>
        <div class="row">
            <div v-for="item in items" :key="item.id" class="col-4">
                <div class="event-card">
                    <h5><a :href="item.url">{{ item.title }}</a></h5>
                    <i class="fa-regular fa-calendar-days"></i><span>{{ item.date }}</span>
                    <p>{{ item.text }}</p>
                    <a :href="item.url">
                        <i class="fa-solid fa-plus"></i>
                        <span>Find More</span>
                    </a>
                </div>
            </div>
        </div>
        <MainButton anchor="View All Events" :url="btnUrl" scheme="regular shadow" />
    </div>
</template>

<script>
import MainButton from './MainButton.vue';
export default {
    name: "EventsCards",
    props: {
        items: Array,
        btnUrl: String,
    },
    components: { MainButton }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

.row {
    margin-bottom: 80px;

    .event-card {
        padding: 40px 30px;
        background-color: #fff;
        color: $light;
        border-radius: 15px;
        position: relative;

        i {
            margin-right: 5px;
        }

        span {
            font-size: 14px;
        }

        h5 a {
            color: $secondary;
        }

        >a {
            background-color: $danger;
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translate(-50%, 50%);
            padding: 10px 20px;
            border-radius: 20px;
            box-shadow: 0 0 20px rgba($color: #000000, $alpha: 0.2);

            &:hover {
                background-color: $primary;
                color: #fff;
            }
        }
    }
}
</style>