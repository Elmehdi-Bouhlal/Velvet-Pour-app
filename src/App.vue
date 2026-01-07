<script setup>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { SplitText } from "gsap/SplitText";
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";

gsap.registerPlugin(ScrollTrigger, SplitText);
</script>

<template>
    <main>
        <Navbar />
        <!-- hero section code -->
        <Hero />
        <div class="h-dvh bg-black"></div>
    </main>
</template>
