<!-- Sezione Latest Courses -->

<template>
    <div class="row">
        <div v-for="item in items" :key="item.id" class="col-3">
            <div class="course-card text-center">
                <a :href="item.url"><img class="course-icon mb-4" :src="require(`../assets/img/${item.icon}`)"
                        :alt="item.name"></a>
                <h6><a class="course-name" href="#">{{ item.name }}</a></h6>
                <div class="course-teacher mb-1"><i class="fa-regular fa-user"></i> Teacher:
                    <strong>{{ item.teacher }}</strong>
                </div>
                <div class="course-price"><i class="fa-regular fa-money-bill-1"></i> Price:
                    <strong>{{ item.price }}</strong>
                </div>
                <a class="course-button" :href="item.url"><i class="fa-solid fa-eye"></i> View Course</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CoursesCards',
    props: {
        items: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

.course-card {
    padding: 40px 0 45px;
    border-radius: 5px;
    position: relative;
    box-shadow: 0 0 20px 1px #F0F0F0;

    i {
        margin-right: 5px;
    }

    .course-icon {
        height: 70px;
    }

    .course-name {
        color: $secondary;

        &:hover {
            color: $danger;
        }
    }

    .course-teacher,
    .course-price,
    .course-button {
        font-size: 14px;
    }


    .course-button {
        background-color: $danger;
        position: absolute;
        left: 50%;
        bottom: 0;
        transform: translate(-50%, 50%);
        font-family: 'Roboto', sans-serif;
        padding: 10px 20px;
        border-radius: 30px;

        &:hover {
            background-color: $primary;
            color: #fff;
        }
    }
}
</style>