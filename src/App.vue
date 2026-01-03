<script setup>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { SplitText } from "gsap/SplitText";
import Navbar from "./components/Navbar.vue";

gsap.registerPlugin(ScrollTrigger, SplitText);
</script>

<template>
    <main>
        <Navbar />
    </main>
</template>
