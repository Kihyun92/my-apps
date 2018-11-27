<template>
    <span class="content-date">
        {{currentDate}}
    </span>
</template>


<script>
import moment from 'moment';

export default {
    name: 'ShowDate',
    data() {
        return {
            currentDate: ''
        }
    },
    methods: {
        initDate() {
            this.currentDate = `${moment().format('dddd')}/${moment().format('LL')}`;
        }
    },
    mounted() {
        this.initDate();
    }
}
</script>


<style>
    .content-date {
        color: #666666;
        float: left;
        font-weight: bold;
        border-bottom: solid 1px black;
    }
</style>
