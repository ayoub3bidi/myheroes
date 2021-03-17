<template>
    <div class="backdrop" @click.self="hideData">
        <div class="data">
            <h1>{{ heroName }}</h1>
            <br>
            <p>{{ description }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Data',
    props: ['heroName', 'description'],
    data() {
        return {
        }
    },
    methods: {
        hideData() {
            this.$emit('hide')
        }
    }
}
</script>

<style scoped>
    .data {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    .backdrop {
        top: 0;
        position: fixed;
        background: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
</style>
