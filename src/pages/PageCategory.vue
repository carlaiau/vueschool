<template>
  <div class="col-full">
    <h1>{{name}}</h1> 
    <CategoryList :categories="categories"/>
  </div>
</template>

<script>
import sourceData from '@/data'
import CategoryList from '@/components/CategoryList'
export default {
    props: {
        id: {
            required: true,
            type: String
        }
    },
    components: {
        CategoryList
    },
    computed: {
        categories () {
            return Object.values(sourceData.forums)
                .filter(forum => forum.categoryId === this.id)
        },
        name () {
            return sourceData.categories[this.id].name
        }
    },
    mounted () {
        console.log(this.id)
    }
}
</script>
