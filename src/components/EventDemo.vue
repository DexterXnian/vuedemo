<template>
    <h3>事件修饰符</h3>
    <a @click.prevent="clickHandle" href="https://baidu.com" >啊</a>
</template>

<script>

export default{
    data(){
        return{

        }
    },
    methods:{
        clickHandle(e){
            // e.preventDefault();
            console.log(e.target);
        }
        
    }
}
</script>