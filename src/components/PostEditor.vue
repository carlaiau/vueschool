<template>
    <form @submit.prevent="save">
        <div class="form-group">
            <textarea
                class="form-input"
                v-model="text"
            ></textarea>
        </div>
        <div class="form-actions">
            <button class="btn-blue">Submit Post</button>
        </div>
    </form>
</template>

<script>

export default {
    data () {
        return {
            thread: this.$store.state.threads[this.id],
            text: ''
        }
    },
    props: {
        threadId: {
            required: true
        }
    },
    methods: {
        save () {
            const post = {
                text: this.text,
                publishedAt: Math.floor(Date.now() / 100),
                threadId: this.threadId,
                userId: 'ALXhxjwgY9PinwNGHpfai6OWyDu2'
            }
            console.log(post)
            this.$store.dispatch('createPost', post)
            this.text = ''
            this.$emit('save', {post})
        }
    }
}
</script>
