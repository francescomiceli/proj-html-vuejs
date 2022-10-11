<!-- Input field -->

<template>
    <div class="input-wrapper">
        <input type="text" :placeholder="placeholder" v-model="inputText">
        <div class="submit-button c-pointer">
            <i :class="['fa-solid', icon, 'submit-icon']"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BaseInput',
    props: {
        icon: String,
        placeholder: String,
    },
    data() {
        return {
            inputText: '',
        }
    },
  
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

.input-wrapper {
    position: relative;

    input {
        width: 100%;
        height: 70px;
        border: 0;
        border-radius: 50px;
        padding-left: 30px;

        &:focus-visible {
            outline: 0;
        }
    }

    .submit-button {
        background-color: $primary;
        height: 70px;
        width: 70px;
        border-radius: 50%;
        color: #fff;
        position: absolute;
        right: 0;
        top: 50%;
        transform: translateY(-50%);

        .submit-icon {
            font: var(--fa-font-solid);
            content: '\f1d8';
            font-size: 20px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        &:hover {
            background-color: $danger;
            box-shadow: 0 0 20px rgba($color: #000000, $alpha: 0.2);
        }
    }
}
</style>