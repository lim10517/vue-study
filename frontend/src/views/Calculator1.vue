<template>
<div>
        <h2>
            기본 계산기
        </h2>
    <div>
        <input type="text" v-model="num1" @keyup="plusNumbers" />
        <span> + </span>
        <input type="text" v-model="num2" @keyup="plusNumbers" />
        <span> = </span>
        <span> {{result}}</span>
    </div>
</div>
</template>

<script>

export default {
    name:'calculator-1',
    data() {
        return {
            num1:0,
            num2:0,
            result :0
        };
    },
    methods : {
        plusNumbers() {
            this.result = parseInt(this.num1) + parseInt(this.num2);
        }
    }
}
</script>
