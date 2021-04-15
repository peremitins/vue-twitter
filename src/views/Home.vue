<template>
  <div class="home">
    <div class="text-white">
      <Tweet v-for="tweet in tweets" :key="tweet._id" :tweet="tweet"></Tweet>
    </div>
  </div>
</template>

<script>
import Tweet from '../components/Tweet'
import { ref } from 'vue';
import vweets from '../vweets';

export default {
  components: { Tweet },
  setup() {
    const tweets = ref(vweets);
    
    return {
      tweets,
      Tweet
    }
  }
}
</script>
