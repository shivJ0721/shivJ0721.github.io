<template>
  <section class="about-section">
    <SectionHeader :text="'ABOUT'" />
    <div class="container">
      <div class="image">
        <p class="disclaimer">
          **A COOL UNSPLASH <br />
          PHOTOGRAPH NOT ME LOL
        </p>
        <div class="image-border"></div>
        <img class="light" alt="Man Looking Up" src="/images/im2.jpg" />
        <img class="dark" alt="Man Looking Up" src="/images/im.jpg" />
      </div>

      <div class="text">
        <p>
          Hi there, I'm Lajat - a seasoned machine learning engineer with a background 
          in full stack development. With a passion for leveraging data-driven insights 
          to solve complex problems, I specialize in developing scalable and robust 
          machine learning models. I have extensive experience in programming languages 
          such as Python, Javascript, and C++, as well as expertise in machine learning 
          libraries such as TensorFlow, Keras, and PyTorch. Additionally, my experience 
          in full-stack development allows me to build seamless and engaging web applications 
          that are both aesthetically pleasing and highly functional. When I'm not busy 
          coding, you can usually find me exploring new technologies, attending tech 
          conferences, competing in CP contests or playing video games. I'm always seeking new challenges and 
          opportunities to learn and grow as a developer. Thanks for stopping by, and I 
          look forward to connecting with you soon!
        </p>

        <button
          @click.prevent="lenis.scrollTo('#contact')"
          type="button"
          class="btn btn_about"
        >
          <span>GET IN TOUCH</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import SectionHeader from "./SectionHeader.vue";
import { lenis } from "../helpers/animations";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
import { onMounted } from "vue";

gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  // // const tl = gsap.timeline({});
  // gsap.from(".about-section .image img", {
  //   y: "50%",
  //   opacity: 0,
  //   duration: 0.5,
  //   ease: "Power3.easeOut",
  //   scrollTrigger: {
  //     trigger: ".about-section .container",
  //     start: "top+=500 bottom",
  //     markers: true,
  //   },
  // });
  // gsap.from(".about-section .text", {
  //   y: "50%",
  //   opacity: 0,
  //   scrollTrigger: {
  //     trigger: ".about-section .container",
  //     start: "top+=500 bottom",
  //     markers: true,
  //   },
  // });
});
</script>

<style lang="scss" scoped></style>
