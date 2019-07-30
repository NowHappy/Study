<template>
    <div>
        <h1 v-if="passedData=='banana'">{{MyMsg}}</h1>
        <h1 v-else>{{passedData}}</h1>
    </div>
</template>

<script>
export default {
    props : {
        passedData: {
                    type: String
                }         
    },
    data() {
        return {
            MyMsg : 'banana is delicous'
        }
    }
}
</script>