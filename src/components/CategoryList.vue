<template>
  <div class="col-full">
    <CategoryListItem 
    v-for="cat in categories" 
    :key="cat['.key']"
    :category="cat"/>
  </div>
</template>

<script>
    import CategoryListItem from '@/components/CategoryListItem'

    export default {
        props: {
            categories: {
                required: true,
                type: Array
            }
        },
        components: {
            CategoryListItem
        }
    }
</script>