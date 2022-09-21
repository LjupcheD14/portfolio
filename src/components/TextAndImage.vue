<template>
  <section>
    <div class="text-and-image" v-for="info in information" :key="info">
      <img class="img-fluid" :src="info.image">
      <div class="tekst col">
        <h1 style="font-weight: bold; font-family: 'Padauk', sans-serif; ">{{info.name_surname}}</h1>
        <p style="font-family: 'Noto Serif', serif; padding: 20px;">
          {{info.text}}
        </p>
      </div>
    </div>

    <div class="text-and-image-mobile" v-for="info in information" :key="info">
      <img class="img-fluid" :src="info.image">
      <div class="tekst-mobile col-mobile p-3">
        <h1 style="font-weight: bold; font-family: 'Padauk', sans-serif; ">{{info.name_surname}}</h1>
        <p style="font-family: 'Noto Serif', serif; padding: 20px;">
          {{info.text}}
        </p>
      </div>
    </div>

    </div>
  </section>
</template>

<script>
export default {
  name: "TextAndImage",
  data(){
    return{
      information: [
        {
          image: require("../assets/images/ljupce.jpg"),
          name_surname: "Ljubomir Davitkov",
          text: "I am a software engineer student who likes to\n" +
              "          upgrade himself constantly with new knowledge and experiences. I would describe myself as a persistent and\n" +
              "          ambitious person because whenever I want something I am going to achieve it. I see myself as a successful\n" +
              "          software engineer in the future."
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
