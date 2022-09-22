<template>

  <main>

    <MetaAndLinks/>
<!--    <TypeWriter/>-->
    <TextAndImage/>
    <Divider/>
    <AboutMe/>
    <Divider/>
    <Footer/>

  </main>
</template>

<style lang="scss">


</style>

<script>

import TextAndImage from "@/components/TextAndImage";
import MetaAndLinks from "@/components/MetaAndLinks";
import AboutMe from "@/components/AboutMe";
import Divider from "@/components/Divider";
import Footer from "@/components/Footer";
// import TypeWriter from "@/components/TypeWriter";

export default {
  components: {
    TextAndImage,
    MetaAndLinks,
    AboutMe,
    Divider,
    Footer
    // TypeWriter
  }
}

</script>
