<template>
    <div id="app">
        <content-header></content-header>
        <content-body></content-body>
    </div>
</template>


<script>
import contentHeader from './components/ContentHeader/ContentHeader';
import contentBody from './components/ContentBody/ContentBody';

export default {
    name: "app",
    components: {
        contentHeader,
        contentBody
    }
};
</script>


<style>
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
