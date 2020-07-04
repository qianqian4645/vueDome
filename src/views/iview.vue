<template>
     <RadioGroup v-model="border">
        <Radio label="金斑蝶" border></Radio>
        <Radio label="爪哇犀牛" border></Radio>
        <Radio label="印度黑羚" border></Radio>
    </RadioGroup>
</template>

<script>
    export default {
        name: '',
        data() {
            return {
                 border: '金斑蝶'
            }
        }
    }
</script>

<style lang="" scoped>
    
</style>