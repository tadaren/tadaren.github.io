<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-square">
        <img :src="skill.imagePath" alt />
      </figure>
    </div>
    <div class="card-header">
      <h4 class="card-header-title">{{ skill.name }}</h4>
    </div>
    <div class="card-content">
      <div class="content">{{ skill.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    skill: Object
  }
};
</script>

<style>
.card-image {
  padding: 10%;
}
</style>
