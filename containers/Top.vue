<template>
    <div id="Top" class="top-content" >
        <h1 id="title">{{ title }}</h1>
        <h2 id="message">{{ message }}</h2>
        <nuxt-link v-scroll-to="'#About'" to>
            <i class="far fa-hand-point-down "></i>
        </nuxt-link>
    </div>
</template>

<script>
export default {
    data (){
        return {
            title: "Welcome to Yosuke's portfolio",
            message: 'Please drag down'
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
    font-family: 'M PLUS Rounded 1c', sans-serif;
}

#title {
    font-size: 4.3em;
    padding: 200px 0 0 0;
    border-bottom: 2px solid white;
}

#message {
     font-size: 3.0em;
     padding: 100px 0 0 0;
}

.far {
    color: white;
    font-size: 3.5em;
    line-height: 150px;
    padding-bottom: 30px;
}

.far:hover {
    opacity: 0.8;
    cursor: pointer;
}

/* タブレット用 */
@media screen and (max-width: 1248px) {
 
    #title {
        font-size: 3.4em;
    }
    #message {
        font-size:  2.5em;
    }

    .far {
        font-size: 3.0em;
    }
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
 
    #title {
        font-size: 2.8em;
    }
    #message {
        font-size:  2.0em;
    }

    .far {
        font-size: 2.6em;
    }
}

</style>