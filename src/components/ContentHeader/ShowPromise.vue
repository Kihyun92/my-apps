<template>
    <div class="promise-container">
        <span class="promise-content"
              v-if="!activateInputBox"
              @click="changeInputBoxFlag">
            다짐 : {{dailyPromiseContent}}
        </span>
        <div class="promise-input-container"
             v-else>
            <input class="promise-input-box"
                   type="text"
                   v-model="inputContent"
                   maxlength="15">
            <button class="submit-button"
                    @click="clickSubmitButton">
                확인
            </button>
            <button class="cancel-button"
                    @click="clickCancelButton">
                취소
            </button>
        </div>
    </div>
</template>


<script>
export default {
    name: 'ShowPromise',
    data() {
        return {
            inputContent: '',
            dailyPromiseContent: 'Always Awake!',
            activateInputBox: false
        };
    },
    methods: {
        changeInputBoxFlag() {
            this.activateInputBox = !this.activateInputBox;
        },
        clickSubmitButton() {
            this.dailyPromiseContent = this.inputContent;
            this.activateInputBox = false;
        },
        clickCancelButton() {
            this.inputContent = '';
            this.activateInputBox = false;
        }
    }
};
</script>


<style>
    .promise-container {
        border-bottom: 1px solid black;
        float: right;
        width: 50%;
    }

    .promise-input-box {
        color: black;
        float: left;
        font-weight: bold;
        font-size: initial;
        width: 80%;
    }

    .promise-content {
        float: left;
        font-weight: bold;
    }
</style>
