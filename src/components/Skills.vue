<template>
  <section class="skills-section" id="skills">
    <SectionHeader :text="'SKILLS'" />
    <div class="skills">
      <div class="skillset--1">
        <h2>
          <span>Javascript</span> . <span>.NET</span> . <span>Django</span> .
          <span>Typescript</span> . <span>Flutter</span> . <span>Flask</span> .
          <span>Javascript</span> . <span>.NET</span> . <span>Django</span> .
          <span>Typescript</span> . <span>Flutter</span> . <span>Flask</span> .
        </h2>
      </div>
      <div class="skillset--2">
        <h2>
          <span>C#</span> . <span>SQL</span> . <span>C++</span> .
          <span>Dart</span> . <span>C</span> . <span>Python</span> .
          <span>C#</span> . <span>SQL</span> . <span>C++</span> .
          <span>Dart</span> . <span>C</span> . <span>Python</span> .
        </h2>
      </div>
      <div class="skillset--1">
        <h2>
          <span>Pytorch</span> . <span>Keras</span> . <span>OpenCV</span> .
          <span>TensorFlow</span> . <span>ScikitLearn</span> . <span>ApacheSpark</span> .
          <span>Pytorch</span> . <span>Keras</span> . <span>OpenCV</span> .
          <span>TensorFlow</span> . <span>ScikitLearn</span> . <span>ApacheSpark</span> .
        </h2>
      </div>
      <div class="skillset--2">
        <h2>
          <span>Git</span> . <span>Kubernetes</span> . <span>Docker</span> .
          <span>AWS</span> . <span>GCP</span> . <span>Azure</span> .
          <span>Git</span> . <span>Kubernetes</span> . <span>Docker</span> .
          <span>AWS</span> . <span>GCP</span> . <span>Azure</span> .
        </h2>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";
import SectionHeader from "./SectionHeader.vue";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: ".skills-section .skills",
      start: "top bottom",
      end: "bottom+=200 top",
      scrub: true,
    },
  });

  tl.fromTo(".skillset--1 h2", { x: "20%" }, { x: "-20%" }, 0).fromTo(
    ".skillset--2 h2",
    { x: "-20%" },
    { x: "20%" },
    0
  );
});
</script>

<style lang="scss" scoped>
@import "@/assets/variables.scss";
</style>
