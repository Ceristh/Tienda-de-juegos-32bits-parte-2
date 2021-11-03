<template>
    <div>
        <div class="form">
        <input type="text" placeholder="Ingresa código" v-model="search" @change="buscar">
        <button @click.prevent="buscar">Buscar</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'input_filtro',
    data: function(){
        return {
            search:'',
        }
    },
    methods: {
        buscar(){
            this.$emit("buscar",{
                search_id:this.search,
            })
        }
    },
}
</script>

<style scoped>
    .form {
        text-align: center;
    }
</style>
