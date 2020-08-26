<template>
  <div>
    <div class="card" @click="isOpen = true">
      <div class="card-header">
        <h4 class="card-header-title is-centered">{{ work.title }}</h4>
      </div>
      <div class="card-image">
        <figure class="image is-16by9">
          <img :src="work.imagePath" alt />
        </figure>
      </div>
    </div>
    
    <b-modal :active.sync="isOpen" :width=640>
      <div class="card">
        <div class="card-header">
          <h4 class="card-header-title">{{ work.title }}</h4>
        </div>
        <div class="card-image">
          <figure class="image is-16by9">
            <img :src="work.imagePath" alt="Image" />
          </figure>
        </div>
        <div class="card-content">
          <div class="content">
            {{ work.content }}
          </div>
        </div>
      </div>
    </b-modal>
  </div>
</template>

<script>
export default {
  props: {
    work: Object
  },
  data() {
    return {
      isOpen: false
    };
  }
};
</script>
