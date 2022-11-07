<script setup lang="ts">
import CardVue from './Card.vue'
import SecondCardListVue from './SecondCardList.vue';
import ThirdCardListVue from './ThirdCardList.vue';
</script>


<template>
<div class="container">
    <Card title="Title" class="card">
      <div class="contents">
        <h2 class="sub">ライトプラン</h2>
        <p class="price">&yen;980(税込)/月</p>
        <div><img src="../assets/light.jpeg" alt="standard_plan_img"></div>
      </div>
    </Card>

    <Card title="Concept" class="card">
      <div class="contents">
        <h2 class="sub">必要最低限でOK&#033;とにかくシンプルなプランをお探しの方に</h2>
        <p>リモートワークやおうち時間が増え、wifi環境でしか携帯を使わない方の為のプラン</p>
        <p>余計なコンテンツを省いた超シンプルプランにしました。</p>
      </div>
    </Card>

    <Card title="Plan" class="card with-text-card">
      <div class="contents plan">
        <h2 class="sub pcg">プラン内容</h2>
        <ul>
          <li>通信量&#058;〜3GB/月</li>
          <li>通話料&#058;〜1時間/月</li>
          <li>携帯故障サポート&#058;無し</li>
        </ul>
      </div>
    </Card>
  </div>
</template>


<style scoped>
.container {
  max-width: 750px;
  display: flex;
  flex-direction: column;
  text-align: center;
  font-size: 13px;
}

.contents {
  margin: 0 auto;
  width: 100%;
}

.contents.plan {
  padding: 20px 0;
  background-color: #f9f9f9;
  border-radius: 8px;
}

.sub {
  font-size: 24px;
}

.sub.pcg {
  margin-top: 0;
}

.card {
  margin-bottom: 8px;
  display: flex;
}

.price {
  font-size: 18px;
  font-weight: bold;
}

img {
  width: 100%;
}

ul {
  margin: 0 auto;
  width: 140px;
  padding-left: 10px;
}

li {
  text-align: left;
}
</style>
