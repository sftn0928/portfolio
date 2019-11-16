<template>
    <div class="title">
        <h2>{{ title }}</h2>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            
        }
    }
}
</script>

<style>
.title {
    margin: 100px 0 50px 0;
    text-align: center;
}

.title h2 {
    border-bottom: 4px solid rgb(255, 163, 25);
    display: inline-block;
    font-family:  Ryumin Medium KL;
    font-size: 3.0em;
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .title h2 {
        font-size: 2.5em;
    }
}
</style>