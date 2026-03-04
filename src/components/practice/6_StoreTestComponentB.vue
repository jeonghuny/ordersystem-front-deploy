<template>
    <h1>stor component B</h1>
    <div>지역변수값 : {{count}}</div>
    <v-btn @click="incrementCount()">지역변수 count값 증가</v-btn>
    <div>전역변수값 : {{getStoredCount}}</div>
</template>

<script>
import { practiceStore } from '@/store/practice';

export default{
    data(){
        return{
            count:0
        }
    },
    computed:{
        getStoredCount(){
            const store = practiceStore(); // 전역 인스턴스 가져옴
            return store.getCount;
        }
    },
    methods:{
        incrementCount(){
            this.count++; // 로컬 count를 증가
        }
    }
}
</script>