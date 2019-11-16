<template>
  <header>
    <div class="header-link">
        <nuxt-link v-scroll-to="'#Top'" to>Top</nuxt-link >
        <nuxt-link v-scroll-to="'#About'" to>About</nuxt-link>        
        <nuxt-link v-scroll-to="'#Career'" to>Career</nuxt-link>
        <nuxt-link v-scroll-to="'#Skill'" to>Skill</nuxt-link>
        <nuxt-link v-scroll-to="'#Works'" to>Works</nuxt-link>
        <nuxt-link v-scroll-to="'#Contact'" to>Contact</nuxt-link>
        <div class="clear" />
    </div>
  </header>
</template>

<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<style>
header {
    background-color: rgb(44, 44, 44);
    position: fixed;
    top: 0;
    z-index: 10;
    width: 100%;
    text-align: center;
}

.header-link {
    cursor: pointer; 
}

.header-link  a {
    display: inline-block;
    line-height: 60px;
    font-size: 25px; 
    width: 120px;
    color: white;
} 

    /* スマートフォン用 */
@media screen and (max-width: 767px) {

  .header-link  a {
    font-size: 16px;
    width: 30%;
    line-height: 30px;
  } 

}
</style>