<template>
  <div>
    <myHeader />
    <Top />
    <About /> 
    <Career />
    <Skill />
    <Works />
    <Contact />
  </div>
</template>

<script>
import myHeader from '@/components/myHeader.vue'
import Top from '@/containers/Top.vue'
import About from '@/containers/About.vue'
import Career from '@/containers/Career.vue'
import Skill from '@/containers/Skill.vue'
import Works from '@/containers/Works.vue'
import Contact from '@/containers/Contact.vue'

export default {
  components: {
    myHeader,
    Top,
    About,
    Career,
    Skill,
    Works,
    Contact
  }
}
</script>

<style>

</style>
