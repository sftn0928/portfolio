<template>
    <div class="about-wrapper">
        <Title title='About' id="About"/>
        <div class="about-content">
            <table class=about-table>
                <tr v-for="(profile,index) in profiles" :key="index">
                    <td  class="about-table-name a-td">
                        {{ profile.name }}
                    </td>
                    <td v-if="profile.url" class="end-td">
                        <a :href="profile.url" target="_blank" ref="noopener">
                            {{ profile.content }}
                        </a>
                    </td>
                    <td v-else class="a-td end-td">
                        {{ profile.content }}
                    </td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    components: {
        Title
    },

    data () {
        return {
            profiles: [
                {name: 'Name', content: '小林 陽佑 (Yosuke Kobayashi)', url: ''},
                {name: 'University', content: '東京電機大学 工学部 情報通信工学科 2年', url: ''},
                {name: 'Birthday', content: '1999/9/28', url: ''},
                {name: 'Mail', content: 'Kobayashi19990928@gmail.com', url: ''},
                {name: 'Twitter', content: '@sftn0928', url: 'https://twitter.com/sftn0928'},
                {name: 'Github', content: 'sftn0928', url: 'https://github.com/sftn0928'}
            ]
        }
    },
}
</script>

<style>
.about-table {
    width: 55%;
    text-align: left;
    font-size: 1.5em;
    margin: 0 auto;
}

.a-td {
    padding: 1% ;
}

.about-table-name {
    font-weight: 500;
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    
    .about-table {
        font-size: 1.1em;
    }

}

</style>