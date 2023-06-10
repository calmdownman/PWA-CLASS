<template>
  <v-container>
    <v-main>
        <div class="text-center display-1 my-4">서브서브 페이지입니다.</div>
        <v-divider></v-divider>
        <!-- 라우터로 전달받은 두개의 매개변수 값을 데이터 속성에 저장한 뒤에 가져와서 표시함 -->
        <div class="text-center display-3 my-4">{{ sTitle1 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle2 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle3 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle4 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle5 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle6 }}</div>
        <div class="text-center">
          <v-btn fab large class="mt-5" color="teal" dark to="/main">
            <v-icon>mdi-replay</v-icon>
          </v-btn>
        </div>
    </v-main>
  </v-container>
</template>

<script>
  export default {
    // 라우터로 전달받은 값을 가져와서 데이터 속성에 저장함
    data() {
      return {
        sTitle1: this.$route.params.p_param1,
        sTitle2: this.$route.params.p_param2,
        sTitle3: this.$route.params.p_param3,
        sTitle4: this.$route.params.p_param4,
        sTitle5: this.$route.params.p_param5,
        sTitle6: this.$route.params.p_param6
      }
    }
  }
</script>