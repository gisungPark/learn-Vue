<template>
  <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
  <app-header v-bind:propsdata="str" v-on:renew="renewStr"></app-header>
</template>

<script>
// 파일의 내용이 AppHeader라는 변수에 담겼다.
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      str: "propsdata",
    };
  },
  components: {
    // import된 변수를 컴포넌트로 등록
    "app-header": AppHeader,
  },
  methods: {
    renewStr: function () {
      this.str = "hi";
    },
  },
};
</script>

<style>
</style>