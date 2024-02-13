<script setup>
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import Subscription from "./ui/Subscription.vue";

const data = [
  {
    id: 1,
    suptitle: "Перед рассветом",
    title: "Утренний бухгалтер",
    imgUrl: "./Picture-1.png",
    descr:
      "Самые важные новости и события за день. Кратко, по делу, структурировано.",
    checkList: [
      "Новости для бухгалтеров, ИП и директора",
      "Подборка статей за день",
    ],
    total: "59 342",
  },
  {
    id: 2,
    suptitle: "После заката",
    title: "Ночной бухгалтер",
    imgUrl: "./Picture-2.png",
    descr:
      "Самая краткая газета о налогах и бухучете в мире — современная рассылка для чтения.",
    checkList: [
      "Анализ, оценка и только самое главное",
      "Лучшие комменты юзеров в обзоре",
    ],
    total: "37 480",
  },
  {
    id: 3,
    suptitle: "Раз в две недели",
    title: "Ножницы скидок",
    imgUrl: "./Picture-3.png",
    descr:
      "Подборка самых выгодных и полезных спецпредложений от надежных компаний.",
    checkList: [
      "Акции и скидки от лидеров рынка",
      "Те, кто подписался – экономят много денег",
    ],
    total: "92 118",
  },
  {
    id: 4,
    suptitle: "По мере появления анонсов",
    title: "Чемодан вебинаров",
    imgUrl: "./Picture-4.png",
    descr:
      "Подборка с анонсами бесплатных вебинаров на самые топовые темы при участии экспертов.",
    checkList: [
      "Никогда не пришлем платные вебинары",
      "Подборка топовых тем для вебинаров",
    ],
    total: "92 082",
  },
];
</script>

<template>
  <Header />
  <main class="p-12 grow bg-[#f5f5f8] rounded-t-2xl max-md:p-3 max-md:pb-6">
    <Subscription />
    <div class="grid grid-cols-2 gap-5 max-md:grid-cols-1 mt-7">
      <Card :data="data" />
    </div>
  </main>
</template>
