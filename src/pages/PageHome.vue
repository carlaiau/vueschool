<template>
  <div class="col-full">
    <h1>Welcome to the forum</h1> 
    <ForumList :forums="forums"/>
  </div>
</template>

<script>
import sourceData from '@/data'
import ForumList from '@/components/ForumList'
export default {
  components: {
    ForumList
  },
  data () {
    const everything = {
      threads: Object.values(sourceData.threads),
      posts: sourceData.posts,
      users: sourceData.users,
      forums: Object.values(sourceData.forums)
    }
    console.log(everything)
    return everything
  }
}
</script>
