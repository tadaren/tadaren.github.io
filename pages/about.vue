<template lang="pug">
  .container
    h2.title.is-2 About
    .columns.is-mobile.is-multiline.is-centered
      figure.image.is-128x128.column.is-narrow
        img.is-rounded(src='~static/icon.png')
      .column.is-10
        h3.title.is-4 ただれん(Tadaren)
        p
          | 私は誰?
        a(href="https://twitter.com/tadaren_s" target="_blank" rel="noopener noreferrer")
          b-icon(icon='twitter' size="is-medium")
        a(href='https://github.com/tadaren' target="_blank" rel="noopener noreferrer")
          b-icon(icon='github' size="is-medium")
      .column.is-12
        h3.title.is-3 Skills
        ul.columns.is-multiline.is-mobile
          li.column.is-2-desktop.is-4-mobile(v-for='skill in skills' :key='skill.name')
            skill(v-bind:skill='skill')
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
          imagePath: '/skills/kotlin.svg',
        },
        {
          name: 'Java',
          content: 'ゲーム制作に使用',
          imagePath: '/skills/java.svg',
        },
        {
          name: 'Python',
          content: '課題や個人用ツールの作成に使用',
          imagePath: '/skills/python.svg',
        },
        {
          name: 'C++',
          content: '競技プログラミングで使用している',
          imagePath: '/skills/c-plusplus.svg',
        }
      ]
    }
  }
}
</script>
