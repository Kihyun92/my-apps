<template>
    <div class="header-container">
        <show-date></show-date>
        <show-promise></show-promise>
    </div>
</template>


<script>
import showDate from './ShowDate';
import showPromise from './ShowPromise';

export default {
    name: 'ContentHeader',
    components: {
        showDate,
        showPromise
    }
}
</script>


<style>
    .header-container {
        position: absolute;
        width: 90%;
        top: 2%;
        padding: 5px 10px;
        /* border : 1px solid #73AD21; */
    }
</style>
