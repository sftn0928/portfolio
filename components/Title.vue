<template>
    <div class="title">
        <h2>{{ title }}</h2>
    </div>
</template>

<script>
export default {
    props: {
        title: String
    }
}
</script>

<style>

.title {
    text-align: center;
    margin-bottom: 60px;
}
.title  h2 {
    border-bottom: 4px solid rgb(255, 163, 25);
    display: inline-block;
    font-family:  Ryumin Medium KL;
    font-size: 2.4em;
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .title h2 {
        font-size: 1.8em;
    }
}
</style>