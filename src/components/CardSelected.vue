<script setup>
import {defineProps} from "vue";

const props = defineProps({
    nome: {
        type: String,
        default: '???',
    },
    xp: {
        type: [String, Number],
        default: ""
    },
    height: {
        type: [String, Number],
        default: ""
    },
    img: {
        type: String,
        default: "https://raw.githubusercontent.com/Jair549/pokevite/a16160030cfc682abb4c7c34843e151acfd5e210/src/assets/egg_pokemon.svg"
    },
    loading: {
        type: Boolean
    }
});
</script>

<template>

<div
    class="card card-selected"
    :class=" loading ? '' : 'animate__animated animate__flipInX' "
    >
    <img height="250" :src="props.img" class="card-img-top pt-2" alt="...">
    <div class="card-body">
        <h5 class="card-title text-center">{{ props.nome }}</h5>
        <hr/>
        <div class="row">
            <div class="col-md-6">
                <strong>XP: </strong>
                <span>{{ props.xp }}</span>
            </div>
            <div class="col-md-6">
                <strong>Altura: </strong>
                <span>{{ props.height }}</span>
            </div>
        </div>
    </div>
</div>
</template>

<style scoped>

.card-selected{
    height: calc(100vh - 140px);
    width: 100%;
    background: rgb(63,237,251);
background: radial-gradient(circle, rgba(63,237,251,1) 0%, rgba(255,5,5,0.4654236694677871) 100%);
}

</style>