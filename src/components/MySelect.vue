<template>
    <div>
        <select class="select-genres" name="genres" id="genres" v-model="valoreDelFiglio">
            <option value="default">Seleziona un genere</option>
            <option value="uno">Seleziona un genere</option>
            <option value="due">Seleziona un genere</option>
        </select>
    </div>
  
</template>

<script>
export default {
    name: 'MySelect',
    data() {
        return {
            valoreDelFiglio: 'default'
        }
    }
}
</script>

<style lang="scss">
    .select-genres {
        margin-right: 10px;
    }
</style>