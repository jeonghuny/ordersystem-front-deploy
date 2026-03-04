<template>
    <!-- 단방향바인딩 : 변수 -> 화면 -->
    <h1>hello world {{language}}</h1>
    <!-- 양방향바인딩 : 변수 -> 화면, 화면 -> 변수 , v-model문법사용(매우 활용도 높음) -->
    <input type="text" v-model="language2">
    <button @click="showValue()">변수확인</button>
</template>

<!-- js의 요소는 script안에 작업-->
<script>
export default {
  data(){
    return{
        language: "java",
        language2: "c++",
    }
  },
    methods:{
        showValue(){
            alert(this.language2);
            console(this.language2);
        }
    }
}
</script>

<!-- css의 요소는 style안에 작업-->
<style>
</style>
