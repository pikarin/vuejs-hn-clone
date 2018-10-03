<template>
  <div class="container">
    <item v-for="story in stories" :key="story" :story="story" />
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
      stories: this.$store.state.newStories
    };
  },
  created() {
    if (this.$store.state.newStories.length === 0) {
      this.$store.dispatch("fetch_new_stories");
    }
  }
};
</script>
