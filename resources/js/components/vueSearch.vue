<template>
    <div class="vueSearch" id="search">
        <input class="input" type="text" v-model="valoreInput" id="input-search" @keypress.13="onClickButton">
        <button class="btn btn-primary" type="button" id="search-btn" @click="onClickButton">Cerca</button>
    </div>
</template>

<script>
    import vueSearch from "../components/vueSearch";
    import vueMain from "../components/vueMain";
    export default {
        // props: {
        //     valoreInput: {
        //         type: String
        //     }                                                          // struttura per inserire i file nei componenti
        components: {
            vueSearch,
            vueMain
        },
        data() {
            return {
                valoreInput: 'Cerca una notizia'
            }
        },
        mounted() {
        },
        computed: {
        },
        methods: {
            onClickButton (event) {
                var value = this.valoreInput;
                this.$emit('clicked', value) // PASSO ILVALORE DAL SEARCH AL MAIN CON EMIT
            }
        }
    }
</script>

<style lang="scss">
  .vueSearch {
    text-align: center;
    .input {
      height: 40px;
      border-radius: 5px;
    }
  }

</style>
