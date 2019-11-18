<template>
    <div clss="works-wrapper">
        <Title title="Works" id="Works"/>
        <div class="works-content">
            <workBox v-for="(content,index) in contents" :key="index" :item="content" />
        </div>
    </div>
</template>

<script>
import Title from '@/components/Title.vue'
import workBox from '@/components/workBox.vue'

export default {
    components: {
        Title,
        workBox
    },

    data (){
        return {
            contents: [
                {
                    imgUrl: require('~/assets/img/portfolio.png'), 
                    title: 'portfolio', 
                    sentence: 'Nuxt.jsで作成したポートフォリオです。', 
                    workUrl: "https://unruffled-mcclintock-bf4292.netlify.com/"
                },
                {
                    imgUrl: require('~/assets/img/stop.png'), 
                    title: '作成中', 
                    sentence: '次回作に期待', 
                    workUrl: ""
                }
            ],

        }
    }
}
</script>

<style>

</style>