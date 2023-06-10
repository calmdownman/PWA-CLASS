<template>
  <v-container>
    <v-main>
        <div class="text-center display-1 my-4">서브 페이지입니다.</div>
        <v-divider></v-divider>
        <!-- 라우터로 전달받은 두개의 매개변수 값을 데이터 속성에 저장한 뒤에 가져와서 표시함 -->
        <div class="text-center display-3 my-4">{{ sTitle1 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle2 }}</div>
        <div class="text-center display-3 my-4">{{ sTitle3 }}</div>
        <v-text-field label="매개변수4" v-model="sParam4"></v-text-field>
        <v-text-field label="매개변수5" v-model="sParam5"></v-text-field>
        <v-text-field label="매개변수6" v-model="sParam6"></v-text-field>
        <div class="text-center">
          <v-btn large class="mt-5" color="purple" dark @click="fnGoSub">
          확 인
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
        sParam4: '',
        sParam5: '',
        sParam6: ''
      }
    },
    methods: {
      // 입력받은 두개의 데이터를 라우터에 저장하여 서브페이지로 이동 및 전달
      fnGoSub() {
        this.$router.push({
          name: 'subsub_page',
          params: {
            p_param1: this.sTitle1,
            p_param2: this.sTitle2,
            p_param3: this.sTitle3,
            p_param4: this.sParam4,
            p_param5: this.sParam5,
            p_param6: this.sParam6
          }
        })
      }
    }
  }
</script>