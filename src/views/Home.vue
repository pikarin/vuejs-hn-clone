<template>
  <div class="container">
    <item v-for="story in stories" :key="story.id" :story="story" />
  </div>
</template>

<script>
import Item from "@/components/Item";

export default {
  name: "home",
  components: { Item },
  data() {
    return {
      err: "",
      stories: this.$store.state.topStories
    };
  },
  created() {
    if (this.$store.state.topStories.length === 0) {
      this.$store.dispatch("fetch_top_stories");
    }
  }
};
</script>
