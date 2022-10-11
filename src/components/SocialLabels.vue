<template>
    <div>
        <a class="social-icon-wrapper" href="#">
            <i class="fa-brands fa-facebook-f"></i>
        </a>
        <a class="social-icon-wrapper" href="#">
            <i class="fa-brands fa-twitter"></i>
        </a>
        <a class="social-icon-wrapper" href="#">
            <i class="fa-brands fa-instagram"></i>
        </a>
    </div>
</template>

<script>
export default {
    name: 'SocialLabels',
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

div {
    margin: 0 -5px;

    .social-icon-wrapper {
        display: inline-block;
        border: 2px solid $primary;
        border-radius: 50%;
        padding: 22px;
        position: relative;
        margin: 0 5px;

        i {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        &:hover {
            background-color: $primary;
            color: #fff;
        }
    }
}
</style>