<template>
  <div class="card h-100 shadow">
    <img 
      :src="icon_url" 
      class="card-img-top" 
      alt="Chuck Norris"
      style="max-height: 200px; object-fit: cover;"
    >
    <div class="card-body">
      <p class="card-text">{{ value }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChuckCard',
  props: {
    icon_url: {
      type: String,
      required: true
    },
    value: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.card {
  transition: transform 0.3s;
  border: none;
  border-radius: 15px;
}

.card:hover {
  transform: translateY(-5px);
}

.card-text {
  font-size: 0.9rem;
  line-height: 1.5;
}
</style>