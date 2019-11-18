<template>
    <div id="Top" class="top-content" >
        <h1 id="title">{{ title }}</h1>
    </div>
</template>

<script>
export default {
    data (){
        return {
            title: "Welcome to Yosuke's portfolio",
        }
    }
}
</script>

<style>
.top-content {
    color: white;
    background-color: rgb(45, 167, 189);
    margin: 0 auto;
    text-align: center;
    background-image: url("../assets/img/top.jpg");
    background-size: contain;
    font-family: 'M PLUS Rounded 1c', sans-serif;
    padding-bottom: 300px;
}

#title {
    font-size: 4.3em;
    padding: 200px 0 0 0;
    border-bottom: 2px solid white;
}

/* タブレット用 */
@media screen and (max-width: 1248px) {
    .top-content {
        background-size: cover;
    }
    
    #title {
        font-size: 3.4em;
    }
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .top-content {
        background-size: cover;
    }

    #title {
        font-size: 2.8em;
    }
}

</style>