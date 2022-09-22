<template>
  <div id="app">
    <typewriter
        :replace="replace"
        :type-interval="100"
        :replace-interval="1000"
    >
      <div>Typewriter Vue</div>
    </typewriter>
  </div>
</template>

<script>

import Typewriter from "typewriter-vue";

export default {
  name: "App",
  components: {
    Typewriter,
  },
  data: () => ({
    replace: [
      { from: "Vue", to: "React?" },
      { from: "Typewriter React?", to: "Joking, it`s Vue!" },
    ],
  }),
};
</script>
