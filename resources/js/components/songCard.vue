<template>
    <div class="products__item">
        <div><img class="roundedImg" :src="image" alt="" width="63" height="63" /></div>
        <div class="products__details">
            <div class="song__author">{{author}}</div>
            <div class="song__title">{{title}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "btnPrimary",
    props: {
        author: {
            type: String,
            default: "Автор неизвестен",
        },
        title: {
            type: String,
            default: "",
        },
        image: {
            type: String,
            default: "",
        }
    }
}
</script>

<style scoped>
    .roundedImg {
        border-radius: 50%;
    }

    .song__author {
        font-weight: 600;
        font-size: 19px;
        line-height: 23px;
        color: #808191;

    }

    .song__title {
        font-weight: 600;
        font-size: 13px;
        line-height: 18px;
        color: #808191;
    }

</style>
