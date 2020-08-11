<template>
    <div class="vueColFooter">
        <ul>
            <li>{{data.name}}</li>
            <li><a :href="data.github">{{data.github}}</a></li>
            <li><a :href="data.linkedin">{{data.linkedin}}</a></li>
        </ul>
    </div>
</template>

<script>
    export default {
            props: ["data"]
    };
</script>

<style lang="scss">
    .vueColFooter {

    }
    ul {
        color: white;
    }
    li {
        list-style: none;
        text-align: center;


    }
    a {
      color: white;
    }
</style>
