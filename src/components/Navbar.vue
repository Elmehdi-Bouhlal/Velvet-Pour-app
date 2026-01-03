<script setup lang="ts">
import { onMounted } from "vue";
import { navLinks } from "../../constants";
import gsap from "gsap";

onMounted(() => {
    const navTween = gsap.timeline({
        scrollTrigger: {
            trigger: "nav",
            start: "bottom top",
        },
    });

    navTween.fromTo(
        "nav",
        {
            backgroundColor: "transparent",
        },
        {
            duration: 1,
            backgroundColor: "#0000050",
            ease: "power1.inOut",
            backgroundFilter: "blur(10px)",
        },
    );
});
</script>

<template>
    <nav>
        <div>
            <a href="#home" class="flex items-center gap-2">
                <img src="/images/logo.png" alt="Logo" />
                <p>Velvet Pour</p>
            </a>
            <ul>
                <li v-for="link in navLinks" :key="link.id">
                    <a :href="`#${link.id}`">{{ link.title }}</a>
                </li>
            </ul>
        </div>
    </nav>
</template>
