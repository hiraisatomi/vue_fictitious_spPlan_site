<script setup lang="ts">
import CardVue from './Card.vue'
import CardList from './CardList.vue';
import ThirdCardListVue from './ThirdCardList.vue';
</script>


<template>
<div class="container">
    <Card title="Title" class="card">
      <div class="contents">
        <p class="tag">おすすめ</p>
        <h2 class="sub">スタンダードプラン</h2>
        <p class="price">&yen;1,980(税込)/月</p>
        <div><img src="../assets/standard.jpeg" alt="standard_plan_img"></div>
      </div>
    </Card>

    <Card title="Concept" class="card">
      <div class="contents">
        <h2 class="sub">値段もパッケージ内容も&quot;ちょうど良い&quot;を求める方へ</h2>
        <p>意外と&quot;ちょうど良い&quot;を突くプランって出逢えないですよね・・</p>
        <p>そんなユーザーの方と同じように&quot;ちょうど良い&quot;プランを求めるスタッフがこのプランを作りました</p>
      </div>
    </Card>

    <Card title="Plan" class="card with-text-card">
      <div class="contents plan">
        <h2 class="sub pcg">プラン内容</h2>
        <ul>
          <li>通信量&#058;〜10GB/月</li>
          <li>通話料&#058;〜5分以内かけ放題/月</li>
          <li>携帯故障サポート&#058;有り</li>
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

h1 {
  font-size: larger;
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
  width: 180px;
  padding-left: 20px;
}

li {
  text-align: left;
}

.tag {
  font-size: 12px;
  margin: 0 auto;
  background-color: rgba(88, 158, 177, 0.7);
  width: 70px;
}

</style>