<script setup>
import { container, item } from "../composables/animation";
const d = new Date();
</script>

<template>
  <main
    class="contain"
    v-motion
    :initial="{ y: '100%' }"
    :enter="{
      y: '0%',
      transition: { duration: 500, ease: 'easeOut' },
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
        Khalid Salman
      </h1>
    </div>
    <!-- Content div -->
    <div class="content">
      <!-- first content -->
      <div
        class="content1"
        v-motion
        :initial="container.hidden"
        :enter="container.show"
      >
        <div class="overflow-hidden">
          <h2 class="" v-motion :initial="item.hidden" :enter="item.show">
            FrontEnd
          </h2>
        </div>
        <div class="overflow-hidden">
          <h2 v-motion :initial="item.hidden" :enter="item.show1">Developer</h2>
        </div>
        <div class="overflow-hidden">
          <h2 v-motion :initial="item.hidden" :enter="item.show1">
            {{ d.getFullYear() }}
          </h2>
        </div>
      </div>
      <!-- second content -->
      <div
        class="content2"
        v-motion
        :initial="container.hidden"
        :enter="container.show"
      >
        <div class="overflow-hidden">
          <h3 v-motion :initial="item.hidden" :enter="item.show">Software Engineer</h3>
        </div>
        <div class="overflow-hidden">
          <h3 v-motion :initial="item.hidden" :enter="item.show1">Lover of Coffee☕</h3>
        </div>
        <div class="overflow-hidden">
          <h3 v-motion :initial="item.hidden" :enter="item.show2">On the path of learning Everything</h3>
        </div>
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
  background: #ffedd5;
  padding-inline: 4rem;
}
.happy {
  margin-top: 10rem;
  margin-bottom: 10rem;
  overflow: hidden;
  padding: 0.25rem;
}
.pickle {
  font-size: 3.75rem;
  text-align: center;
}

.content {
  display: flex;
  justify-content: space-between;
}

.content1 {
  text-align: left;
  font-size: 1.5rem;
}
.content2{
  text-align: right;
  font-size: 1rem;
}

@media screen and (min-width: 1024px) {
  .pickle {
    text-align: right;
    font-size: 8rem;
  }
  .happy {
    margin-bottom: 5rem;
  }
  .content1 {
    font-size: 3.75rem;
  }
  .content2{
    
    font-size: 1.5rem;
  }
}

.overflow-hidden {
  overflow: hidden;
}
</style>
