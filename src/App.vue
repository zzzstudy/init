<!--  -->
<template>
    <div @click="onhandele()">
        {{ obj.msg }}
        {{ name }}
    </div>
</template>

<script>
import { reactive, toRef, toRefs } from 'vue';
export default {
    name: 'App',

    setup() {

        const obj = reactive({
            msg: 'nihao vue3',
            name: 'zhangsan',
            age: 18
        })
        const name = toRef(obj, 'name')

        const onhandele = () => {
            obj.msg = 'vue'
            name.value = 'lisi'

        }

        return { onhandele, obj, name }
    }

}
</script>