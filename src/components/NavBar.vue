<script setup lang="ts">
import { siteConfig } from '~/config'
</script>

<template>
  <header class="z-40 text--c-text">
    <router-link
      to="/"
      focusable="false"
      class="absolute m-6 h-10 w-10 select-none outline-none lg:fixed"
    >
      <img
        :src="`/favicon${isDark ? '-dark' : ''}.svg`"
        alt="favicon"
      >
    </router-link>
    <nav class="flex flex-row items-center gap-5 p-8">
      <div class="grow" />
      <router-link to="/" title="Home">
        <span class="lt-md:hidden">Home</span>
        <div class="i-carbon:home md:hidden" aria-hidden="true" />
      </router-link>
      <router-link to="/projects" title="Projects">
        <span class="lt-md:hidden">Projects</span>
        <div class="i-ri-code-s-slash-line md:hidden" aria-hidden="true" />
      </router-link>
      <!-- <router-link to="/posts" title="Blog">
        <span class="lt-md:hidden">Blog</span>
        <div class="i-ri-article-line md:hidden" />
      </router-link> -->
      <router-link to="/resume" title="Resume">
        <span class="lt-md:hidden">Resume</span>
        <div class="i-uil-file-alt md:hidden" aria-hidden="true" />
      </router-link>
      <a
        :href="`https://github.com/${siteConfig.github}`"
        title="GitHub"
        target="_blank"
        rel="noopener"
        class="custom-icon-btn"
      >
        <div class="i-carbon:logo-github w-6 h-6" />
      </a>
      <a
        :href="`https://linkedin.com/in/${siteConfig.linkedin}`"
        title="LinkedIn"
        target="_blank"
        rel="noopener"
        class="custom-icon-btn"
      >
        <div class="i-carbon:logo-linkedin w-6 h-6" />
      </a>
      <a
        :href="`mailto:${siteConfig.email}`"
        title="Email"
        target="_blank"
        rel="noopener"
        class="custom-icon-btn"
      >
        <div class="i-carbon:email w-6 h-6" />
      </a>
      <a
        title="Toggle Color Scheme"
        class="custom-icon-btn"
        @click="toggleTheme()"
      >
        <div class="i-carbon:sun dark:i-carbon:moon w-6 h-6" />
      </a>
    </nav>
  </header>
</template>

<style scoped>
nav a {
  transition: opacity 0.2s ease;
  opacity: 0.6;
}

nav a:hover {
  opacity: 1;
}
</style>
