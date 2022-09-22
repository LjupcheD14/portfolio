<template>

  <main>

    <MetaAndLinks/>
    <TypeWriterExample/>
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

export default {
  components: {
    TextAndImage,
    MetaAndLinks,
    AboutMe,
    Divider,
    Footer
  }
}

</script>
