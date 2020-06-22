<template>
  <div clss="Skill-wrapper">
    <Title title="Skill" id="Skill" />
    <SkillType :items="skills" />
  </div>
</template>

<script>
import Title from "@/components/Title.vue";
import SkillType from "@/components/SkillType.vue";
export default {
  components: {
    Title,
    SkillType
  },
  data() {
    return {
      skills: [
        {
          svg: require("@/assets/icons/html5.svg"),
          name: "HTML",
          level: "★★★",
          career: "2019.7 ~"
        },
        {
          svg: require("@/assets/icons/css3.svg"),
          name: "CSS",
          level: "★★★",
          career: "2019.7 ~"
        },
        {
          svg: require("@/assets/icons/javascript.svg"),
          name: "JavScript",
          level: "★★★",
          career: "2019.8 ~"
        },
        {
          svg: require("@/assets/icons/vue.svg"),
          name: "Vue.js",
          level: "★★☆",
          career: "2020.2 ~"
        },
        {
          svg: require("@/assets/icons/nuxt.svg"),
          name: "Nuxt.js",
          level: "★★☆",
          career: "2020.2 ~"
        },
        {
          svg: require("@/assets/icons/react.svg"),
          name: "React.js",
          level: "★☆☆",
          career: "2020.5 ~"
        },
        {
          svg: require("@/assets/icons/nodejs.svg"),
          name: "Node.js",
          level: "★☆☆",
          career: "2020.4 ~"
        },
        {
          svg: require("@/assets/icons/php.svg"),
          name: "PHP",
          level: "★☆☆",
          career: "2020.5 ~"
        },
        {
          svg: require("@/assets/icons/java.svg"),
          name: "Java",
          level: "★☆☆",
          career: "2019.4 ~"
        },
        {
          svg: require("@/assets/icons/c.svg"),
          name: "C",
          level: "★☆☆",
          career: "2018.4 ~"
        },
        {
          svg: require("@/assets/icons/bootstrap.svg"),
          name: "Bootstrap",
          level: "★★★",
          career: "2019.10 ~"
        },
        {
          svg: require("@/assets/icons/aws.svg"),
          name: "AWS",
          level: "★☆☆",
          career: "2020.5 ~"
        }
        // {svg:require("@/assets/icons/docker.svg") , name: 'Docker', level: '★☆☆', career: "2020. ~"},
        // {svg:require("@/assets/icons/mysql.svg") , name: 'mySQL', level: '★☆☆', career: "2020. ~"},
        // {svg:require("@/assets/icons/.svg") , name: '', level: '★★☆', career: "2020. ~"},
      ]
    };
  }
};
</script>

<style></style>
