<template>
  <div class="container">
    <p style="font-family: 'Noto Serif', serif; padding-left: 10px;">
      <span class="typed-text">{{ typeValue }}</span>
      <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>
    </p>
  </div>
</template>

<script>
// import { setTimeout } from 'timers';
export default {
  data: () => {
    return {
      typeValue: '',
      typeStatus: false,
      typeArray: ['Computer science student', 'Intern at Bike Computer'],
      typingSpeed: 50,
      erasingSpeed: 50,
      newTextDelay: 500,
      typeArrayIndex: 0,
      charIndex: 0
    }
  },
  methods: {
    typeText() {
      if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if(!this.typeStatus)
          this.typeStatus = true;
        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      }
      else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if(this.charIndex > 0) {
        if(!this.typeStatus)
          this.typeStatus = true;
        this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      }
      else {
        this.typeStatus = false;
        this.typeArrayIndex += 1;
        if(this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    }
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  }
}
</script>

<style scoped>
@keyframes blink {
  from,
  to {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}
.content *:last-child::after {
  font-size: calc(1em + 2px);
  content: "|";
  animation: blink 0.75s step-end infinite;
}
</style>
