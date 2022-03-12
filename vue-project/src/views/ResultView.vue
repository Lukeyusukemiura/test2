<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HeaderAll from "@/components/HeaderAll.vue";
</script>

<template>
  <!-- ヘッダーの追加　-->
  <HeaderAll />
    <!--背景が黄色の一番大本の箱-->
   <div class="box bg-yellow-500">

    <!--スコアの箱-->
    <div class="pt-20 flex items-center justify-center pb-10">
      <p class="text-6xl font-bold">スコア : 100</p>
    </div>

    <!--「時間」「ミスタイプ」「苦手キー」の箱-->
    <div class="pt-5 flex items-center justify-center">
      <ol class="resultbox text-center">
        <li class="text-2xl">時間: 3.23</li>
        <li class="text-2xl">ミスタイプ数：</li>
        <li class="text-2xl">苦手キー:</li>
      </ol>
    </div>

    <!--ツイッターでシェアの箱-->
    <div class="pt-10 flex items-center justify-center">
      <p class="text-4xl twitterbox text-center">Twitter でシェア</p>
    </div>

    <!--「メインに戻る」と「リスタート」のボタンを格納-->
    <div class="pt-20 pb-20 flex items-center justify-center">
      <div class="flex buttonbox justify-around">
        <RouterLink class="inline-block px-20 py-3 rounded-lg shadow-lg bg-indigo-700 text-white" to="/">メインに戻る</RouterLink>
        <a href="#" class="inline-block px-20 py-3 rounded-lg shadow-lg bg-gray-600 text-white">リスタート</a>
      </div>
    </div>

  </div>
</template>

<style>
.box{
  height:91.7vh;
  width: 100%;
}

.resultbox{
  width: 250px;
}

.twitterbox{
  width:350px;
}

.buttonbox{
  width:800px;
}
</style>


