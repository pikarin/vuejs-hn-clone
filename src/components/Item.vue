<template>
  <div class="story">
    <span class="score">{{ story.data.score }}</span>
    <router-link :to="{ path: '/story/' + story.data.id }">
      {{ story.data.title }}<span>{{ story.data.url | host }}</span>
    </router-link>
    <br />
    <span class="meta">
      by {{ story.data.by }} | {{ story.data.time }} Ago | {{ story.data.descendants }} comments
    </span>
  </div>
</template>

<script>
export default {
  name: "Item",
  props: ["story"]
};
</script>

<style lang="scss" scoped>
.story {
  background-color: #ffffff;
  padding: 20px 30px 20px 80px;
  border-bottom: 1px solid #eeeeee;
  position: relative;
  line-height-step: 20px;

  a {
    color: #34495e;
    font-weight: 600;
    text-decoration: none;

    span {
      font-size: 0.85em;
      margin-left: 10px;
      color: #828282;
    }
  }

  .meta {
    font-size: 0.85em;
    color: #828282;
  }
}
.score {
  color: #ff6600;
  font-size: 1.1em;
  font-weight: 700;
  position: absolute;
  top: 50%;
  left: 0;
  width: 80px;
  text-align: center;
  margin-top: -10px;
}
</style>
