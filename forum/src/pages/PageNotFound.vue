<template>
  <div class="col-full" :class="$style.centered">
    <h1 :class="$style.headingLarge">Sorry this does not exist</h1>
    <p :class="$style.bodyLarge">
        Why don't you go 
        <router-link :to="{name:'Home'}">
            home
        </router-link> 
        instead?
    </p>
  </div>
</template>

<script>
    export default{}
</script>

<style module>
    .headingLarge{
        font-size: 50px;
    }
    .bodyLarge{
        font-size: 20px;
        font-weight: 100;
    }
    .centered{
        text-align: center;
    }
</style>