<template>
  <div class="container">
    <h2 class="title is-2">About</h2>
    <div class="columns is-mobile is-multiline is-centered">
      <figure class="image is-128x128 column is-narrow">
        <img class="is-rounded" src="icon.png" />
      </figure>
      <div class="column is-10">
        <h3 class="title is-4">ただれん(Tadaren)</h3>
        <p>
          私は誰?
        </p>
      </div>
      <div class="column is-12">
        <h3 class="title is-3">Skills</h3>
        <ul class="columns is-multiline is-mobile">
          <li v-for="skill in skills" :key="skill.name" class="column is-2-desktop is-half-mobile">
            <skill v-bind:skill="skill"></skill>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Skill from '~/components/Skill.vue';

export default {
  components: {
    Skill,
  },
  data() {
    return {
      skills: [
        {
          name: 'Kotlin',
          content: '研究でも使用した言語で一番好きな言語',
          imagePath: 'skills/kotlin.svg',
        },
        {
          name: 'Java',
          content: 'ゲーム制作に使用',
          imagePath: 'skills/java.svg',
        },
        {
          name: 'Python',
          content: '課題や個人用ツールの作成に使用',
          imagePath: 'skills/python.svg',
        },
        {
          name: 'C++',
          content: '競技プログラミングで使用している',
          imagePath: 'skills/c-plusplus.svg',
        }
      ]
    }
  }
}
</script>
