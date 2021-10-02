<template>
    <div>
        <h1>想你了</h1>
        <button @click="count++">{{count}}次</button>
    </div>
</template>
<script>
export default {
    name:'',
    data() {
        return {
            count:0
        }
    },
}
</script>