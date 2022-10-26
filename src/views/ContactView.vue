<script setup>
import { container, item } from "../composables/animation";
</script>
<template>
  <main
    class="contain"
    v-motion
    :initial="{ y: '100%' }"
    :enter="{
      y: '0%',
      transition: { duration: 75, ease: 'easeOut' },
    }"
    :leave="{
      opacity: 1,
    }"
  >
    <!-- Title div -->
    <div class="happy">
      <h1
        v-motion
        :initial="{ y: 100 }"
        :enter="{
          opacity: 1,
          y: 0,
          transition: { delay: 0.5, duration: 300 },
        }"
        class="pickle"
      >
        Let's Talk
      </h1>
    </div>
    <!-- Content div -->
    <div class="content">
      <div v-motion :initial="container.hidden" :enter="container.show">
        <div class="find">
          <h4 v-motion :initial="item.hidden" :enter="item.show">Find Me:</h4>
        </div>
      </div>
      <div class="links">
        <ul v-motion :initial="container.hidden" :enter="container.show">
          <div class="overflow-hidden">
            <li v-motion :initial="item.hidden" :enter="item.show">
              <a href="https://twitter.com/salskhal" target="blank">Twitter</a>
            </li>
          </div>
          <div class="overflow-hidden">
            <li v-motion :initial="item.hidden" :enter="item.show1">
              <a href="">Github</a>
            </li>
          </div>
          <div class="overflow-hidden">
            <li v-motion :initial="item.hidden" :enter="item.show2">
              <a href="">Linkedin</a>
            </li>
          </div>
        </ul>
      </div>
    </div>
  </main>
</template>
<style scoped>
.contain {
  color: #0f172a;
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: #f87171;
  padding-inline: 4rem;
}
.happy {
  margin-top: 10rem;
  margin-bottom: 10rem;
  overflow: hidden;
  padding: 0.25rem;
}

.content {
  display: flex;
  justify-content: space-between;
}
.pickle {
  font-size: 3.75rem;
  text-align: center;
}

.find {
  font-size: 1rem;
  overflow: hidden;
}

.links {
  font-size: 1.5rem;
  text-decoration: underline;
}

ul {
  list-style: none;
}

a {
  color: #0f172a;
}

@media screen and (min-width: 1024px) {
  .happy {
    margin-bottom: 5rem;
  }
  .pickle {
    text-align: right;
    font-size: 8rem;
  }
  .find {
    font-size: 1.5rem;
  }
  .links {
    font-size: 3.75rem;
  }
}

.overflow-hidden {
  overflow: hidden;
}
</style>
