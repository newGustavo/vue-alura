<script lang="ts">
import Tag from './Tag.vue';
    export default {
    data() {
        return {
            selecionado: false
        }
        },
    props: {
        ingrediente: {type: String, required: true}
    },
    components: { Tag }
    }
</script>

<template>
    <button
    @click="selecionado = !selecionado"
    class="ingrediente"
    >
        <Tag :texto="ingrediente" :ativa="selecionado" />
    </button>
</template>

<style scoped>
.ingrediente{
    cursor: pointer;
}
</style>