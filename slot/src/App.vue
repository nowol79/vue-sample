<template>
  <div id="app">
    <twice-card :headerText="A.header" :footerText="A.footer">
      <div>
        <p><img :src="A.message" alt="나연 이미지"></p>
      </div>
    </twice-card>
    <twice-card class="sanders" :headerText="B.header" :footerText="B.footer">
      <div>
        <p><img :src="B.message" alt="정연 이미지"></p>
      </div>
    </twice-card>
    <twice-card class="sanders" :headerText="C.header" :footerText="C.footer">
      <div>
        <p><img :src="C.message" alt="모모 이미지"></p>
      </div>
    </twice-card>
      <br>
    <twice-card class="sanders" :headerText="D.header">
      <div>
        <p v-html="D.message"> {{ D.message }}</p>
      </div>
    </twice-card>
  </div>
</template>

<script>
import TwiceCard from './components/TwiceCard.vue'

export default {
  name: 'app',
  components: {
    TwiceCard
  },
  data: function() {
    return {
      A: {
        header: "나연이미지",
        footer: "출처: 네이버",
        message: 'https://search.pstatic.net/common/?src=http%3A%2F%2Fsstatic.naver.net%2Fpeople%2Fportrait%2F201812%2F20181204121055605-4854115.jpg'
      },
      B: {
        header: "정연이미지",
        footer: "출처: 네이버",
        message: "https://search.pstatic.net/common/?src=http%3A%2F%2Fsstatic.naver.net%2Fpeople%2Fportrait%2F201812%2F20181204121414902-2803926.jpg"
      },
      C: {
        header: "모모이미지",
        footer: "출처: 네이버",
        message: "https://search.pstatic.net/common/?src=http%3A%2F%2Fsstatic.naver.net%2Fpeople%2Fportrait%2F201812%2F20181204121518422-6151793.jpg"
      },
      D: {
        header: "나연신상",
        message: "<table><tr><td>데뷔</td><td>2015.10.20|한국</td></tr><tr><td>장르</td><td>가요</td></tr></table>"
      },
    };
  }
}
</script>

<style scoped>
.sanders { background-color: antiquewhite; }
.sanders-content { font-family: 굴림; text-decoration: underline;}
</style>
