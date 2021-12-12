<template>
     <div>
         <span>姓名：{{name}}</span><br>
         <span>性别：{{gender}}</span>
         <button @click="changeInfo">修改信息</button>
     </div>
</template>

<script>
import {  reactive, toRefs } from 'vue';
export default {
    async setup(){
        let info = reactive({
            name:"N+",
            gender:1
        })
        let changeInfo = () => {
            info.name = "聂少"
        }
        let newObj = await new Promise((resolve,reject)=>{
            setTimeout(() => {
             resolve(toRefs(info))
            }, 3000);
        })
        return{
            ...newObj,changeInfo
        }
    }
}
</script>
