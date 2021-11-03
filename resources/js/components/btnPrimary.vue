<template>
    <button class="btn__primary" @click="clickButton">
        <span class="icon__plus" v-if="showIcon"></span>
        <span>{{sign}}</span>
    </button>
</template>

<script>
export default {
    name: "btnPrimary",
    props: {
        sign: "",
        showIcon: false
    },
    methods: {
        clickButton () {
            this.$emit("btnPrimaryClick");
        }
    }
}
</script>

<style scoped>
    .btn__primary {
        display: flex;
        align-items: center;
        background-color: #6C5DD3;
        border-radius: 12px;
        border: none;
        padding: 13.5px 13px;
        font-size: 14px;
        font-weight: 600;
        color: #FFFFFF;
    }

    .icon__plus {
        display: block;
        width: 21px;
        height: 21px;
        background-image: url(../img/add_track_btmPrimary.svg);
        background-size: contain;
        margin-right: 10px;
    }
</style>
