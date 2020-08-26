<template>
  <div class="container">
    <h2 class="title is-2">Works</h2>
    <ul class="columns is-multiline is-centerd">
      <li v-for="work in works" :key="work.title" class="column is-4">
        <work v-bind:work="work"></work>
      </li>
    </ul>
  </div>
</template>

<script>
import Work from '@/components/Work.vue';

export default {
  components: {
    Work
  },
  data() {
    return {
      works: [
        {
          title: 'レーザーハープ',
          content: '何か書く',
          imagePath: 'work/harp.png'
        },
      ]
    }
  }
}
</script>
