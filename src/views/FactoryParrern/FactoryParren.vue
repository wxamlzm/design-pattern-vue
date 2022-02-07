<template>
    <form action="">
        <InputFactory v-for="item in inputList" :type="type" :status="status" :key="item"> </InputFactory>
    </form>
</template>

<script>
// 引入组件
import InputFactory from './InputFactory';
// 工厂模式练习
export default {
    name: 'Form',
    props: {
        type: '',
    },
    computed: {
        inputList() {
            return formMap[this.type];
        },
    },
    components: {
        InputFactory,
    },
};
</script>
