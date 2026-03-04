<template>
    <v-btn>라우트3 화면</v-btn>
</template>
<script>
export default{
    data(){
        return{
            id: null,
        }
    },
    created(){
        this.id = this.$route.params.productId;
        console.log(this.id);
        // 아래와 같이 라우터를 통해 전달된 id값을 꺼내어 서버로 데이터 요청
        // const result = axios.get("http://localhost:8080/product/deail/" + this.id);
        // console.log(result);
    },
    methods: {

    }
}
</script>