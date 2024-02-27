<template>
    <div>
        <p>Somethisn here</p>     
        <div class="testingo">{{ text_var }}</div>   
    </div>
</template>

<script>
export default {
    data() {
        return {
            text_var: "this is the text in the var"
        };
    }
};
</script>

<style>
.testingo {
    font-size: 2rem;
    color: green;
    margin: 24rem;
}
</style>