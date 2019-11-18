<template>
    <div clss="Skill-wrapper">
        <Title title="Skill" id="Skill"/>
        <div class="skill-content">
            <table class="skill-table">
                <tr v-for="(skill,index) in skills" :key="index">
                    <td align="left" class="skill-name st">{{ skill.name }}</td>
                    <td class="star st">{{ skill.level }}</td>
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
    data (){
        return {
            skills: [
                {name: 'HTML', level: '★★★'},
                {name: 'CSS', level: '★★★'},
                {name: 'Javascript', level: '★★☆'},
                {name: 'Vue.js/Nuxt.js', level: '★☆☆'},
                {name: 'C', level: '★☆☆'},
                {name: 'Java', level: '★☆☆'},
                {name: 'Bootstrap', level: '★★☆'},
                {name: 'Github', level: '★☆☆'},
            ]
        }
    }
}
</script>

<style>

.skill-name {
    font-size: 1.5em;
}

.star {
    font-size: 1.9em;
    color: rgb(255, 217, 0);
}

.skill-table {
    margin: 0 auto;
    width: 30%;
}

.st {
    padding: 0 12%;
}

/* タブレット用 */
@media screen and (max-width: 1248px) {
    .skill-name {
        font-size: 1.3em;
    }
    .star {
        font-size: 1.7em;
    }
    .skill-table {
        width: 55%;
    }
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
    .skill-name {
        font-size: 1.1em;
    }

    .star {
        font-size: 1.5em;
    }

    .skill-table {
        width: 50%;
    }

    .st {
        padding: 0 10%;
    }
}

</style>