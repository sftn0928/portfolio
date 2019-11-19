<template>
    <div class="career-wrapper">
        <Title title='Career' id="Career"/>
        <div class="career">
            <b-table :items="career_content" :fields="career_fields"></b-table>
        </div>
    </div>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    components: {
        Title
    },

    data (){
        return{
            career_fields: ['年','月','内容'],
            career_content: [
                {年: '2018', 月: '4', 内容: '東京電機大学 工学部 情報通信工学科 入学'},
                {年: '2019', 月: '5', 内容: '基本情報技術者試験 合格' },
                {年: '2019', 月: '5', 内容: '学生エンジニア団体 steg 加入' },                
            ]       
        }
    }
}
</script>

<style>
.career {
    text-align: left;
    font-size: 1.3em;
    margin: 0 auto;
    width: 55%; 
}

/* タブレット用 */
@media screen and (max-width: 1248px) {
   .career{
        font-size: 1.3em;
        width: 65%;
    }
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .career{
        font-size: 1em;
        width: 70%;
    }
}
</style>