<script setup>
import { ref, computed } from 'vue';
const props = defineProps(['title', 'content'])

const shoBox = ref(false)

const TextoBotao = computed(() =>
    shoBox.value ? 'Esconder' : ' Mostrar'
);
</script>

<template>
    <div>
        <button @click="shoBox = !shoBox"> {{ TextoBotao }}</button>
        <div v-if="shoBox" class="Expande-box">
            <h1>{{ props.title }}</h1>
            <h6>{{ props.content }}</h6>
           <p> vargas o mais foda do if</p>

        </div>
    </div>
</template>

<style scoped>
.Expande-box {
    height: 100%;
    width: 400px;
    padding: 20px;
    border-radius: 10px;
    border: 1px solid black;
    box-shadow: 3px 3px 2px 2px gray;

}





;
</style>
