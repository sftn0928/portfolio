<template>
    <div class="work-box">
        <div class="work-cord">
            <div><img :src="item.imgUrl" alt="イメージ画像" ></div>
            <div class="work-card-content">
                <h3 class="card-title">{{ item.title }}</h3>
                <p class="card-sentence">{{ item.sentence }}</p>
                <a :href="item.workUrl" class="detail btn btn-outline-info" 
                    target="_blank" rel="noopner">詳細</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        item: { 
            
        },
    }
}
</script>

<style>
.work-box {
    text-align: center;
}

.work-cord {
    margin: 50px auto;
    width: 50%;
    border: 1px solid gray;
}

.card-title {
    padding-top: 15px;
}

.work-card-content {
    border-top: 1px solid gray;
}

.detail {
    margin: 10px 0;
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .work-cord {
        width: 75%;
        font-size: 0.8em;
    }
    .card-title {
       font-size: 1.5em;
    }
}
</style>