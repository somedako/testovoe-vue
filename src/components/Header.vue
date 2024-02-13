<script setup>
import Logo from "../ui/Logo.vue";
import BreadCrumb from "../ui/Breadcrumb.vue";
import Nav from "./Nav.vue";
import LogoIcon from "/klerk.svg";

const breadCrumbs = [
  { title: "Главная", link: "/" },
  { title: "Рассылки", link: "/" },
  { title: "Хлебные крошки", link: "/" },
];

const navigations = [
  { name: "Рассылки", link: "/mailings", isActive: true },
  { name: "Соцсети", link: "/mailings", isActive: false },
  { name: "Мессенджеры", link: "/massengers", isActive: false },
];
</script>

<template>
  <header class="bg-[#fff] pt-8">
    <Logo :logo="LogoIcon" />
    <BreadCrumb :breadCrumbs="breadCrumbs" />
    <h1 class="text-center mt-5 font-semibold text-5xl max-md:text-3xl">
      Подписки «Клерка»
    </h1>
    <Nav :navigations="navigations" />
  </header>
</template>
