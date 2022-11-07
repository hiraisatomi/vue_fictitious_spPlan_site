<script setup lang="ts">
import { ref, computed } from 'vue'
import CardList from './components/CardList.vue';
import SecondCardList from './components/SecondCardList.vue';
import ThirdCardList from './components/ThirdCardList.vue';

const ActiveTabName = ref('1')
const updateTab = (activeName: string) => {
  ActiveTabName.value = activeName
}

const currentComponent = computed(() => {
  switch (ActiveTabName.value) {
    case '1':
      return CardList
    case '2':
      return SecondCardList
    case '3':
      return ThirdCardList
    default:
      return CardList
  }
})
</script>


<template>
  <h1>プランのご案内</h1>
  <div class="tab_changer">
    <button class="tab_btn" @click="updateTab('1')"><p class="tab_concept">シンプル安さが魅力</p>ライトプラン</button>
    <button class="tab_btn" @click="updateTab('2')"><p class="tab_concept">ちょうど良い が詰まった</p>スタンダードプラン</button>
    <button class="tab_btn" @click="updateTab('3')"><p class="tab_concept">充実の内容と保証</p>ハイスペックプラン</button>
  </div>
  <div class="tab_contents">
    <component :is="currentComponent"></component>
  </div>
</template>


<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow: hidden;
}

h1 {
  font-size: 36px;
}

.tab-contents {
  margin-top: 30px;
}

.tab_btn {
  margin: 10px 15px;
  width: 200px;
}

.tab_concept {
  font-size: 10px;
}
</style>
