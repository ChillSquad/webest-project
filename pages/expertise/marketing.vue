<script setup>
import Advantages from "~/components/ExpertisePage/Advantages.vue";
import ExpertiseHeading from "~/components/ExpertisePage/ExpertiseHeading.vue";
import Priority from "~/components/ExpertisePage/Priority.vue";
import BlogUnit from "~/components/BlogPage/BlogUnit.vue";
import Recruiting from "~/components/ExpertisePage/Recruiting.vue";
import CustomersUnit from "~/components/CustomersPage/CustomersUnit.vue";
import TalkUnit from "~/components/TalkPage/TalkUnit.vue";
import ArticleSlider from "~/components/UI-kit/ArticleSlider.vue";
import ArticleSliderMobile from "~/components/UI-kit/ArticleSliderMobile.vue";

const breadcrumbItems = [
  { label: "Назад ко всем услугам", route: "/expertise" },
];

const cards = [
  {
    src: "/images/imageMarketing2.png",
    title: "Контекстная реклама Яндекс Директ и Google Ads",
  },
  {
    src: "/images/imageMarketing3.png",
    title: "Таргетированная реклама",
    subtitle:
      "ВК, MyTarget, Facebook/Instagram, МТС Маркетолог, СберТаргет, Билайн Таргет",
    wide: true,
  },
  {
    src: "/images/imageMarketing4.png",
    title: "SEO-продвижение сайтов в Яндекс и Google",
  },
  {
    src: "/images/imageMarketing5.png",
    title: "Продвижение в сервисах Яндекс",
    subtitle:
      "Яндекс.Бизнес, Яндекс.Геореклама (Яндекс.Навигатор, Яндекс.Карты)",
    tall: true,
  },
  {
    src: "/images/imageMarketing6.png",
    title: "Продвижениена маркетплейсах",
    subtitle: "Wildberries, Яндекс Маркет, OZON",
  },
  {
    src: "/images/imageMarketing7.png",
    title: "Email-маркетинг",
  },
  {
    src: "/images/imageMarketing8.png",
    title: "Контент-маркетинг",
    subtitle:
      "Яндекс.Бизнес, Яндекс.Геореклама (Яндекс.Навигатор, Яндекс.Карты)",
  },
];

const priorityItems = [
  {
    heading: "Гибкий форматы работы",
    content:
      "Мы предлагаем как классический аутсорсинг и аутстаффинг, так и различные комбинации, оптимальные для вашего бизнеса",
  },
  {
    heading: "Эффективные методы разработки",
    content:
      "Вы можете выбрать для себя наиболее подходящую методологию - Scrum или Waterfall",
  },
  {
    heading: "Современные технологии",
    content:
      "Мы используем новейшие технологии, такие как Bitrix, VueJs и Laravel",
  },
  {
    heading: "Собственный отдел аналитики и дизайна",
    content:
      "Мы делаем продукты, которые соответствуют нуждам наших клиентов и максимально легко используются конечным пользователем",
  },
  {
    heading: "Тестирование на всех этапах разработки",
    content:
      "Улучшение качества конечного продукта за счёт более эффективной работы и использования ресурсов",
  },
  {
    heading: "Сертификация крупных корпоративных внедрений",
    content:
      "Мы делаем продукты, которые соответствуют нуждам наших клиентов и максимально легко используются конечным пользователем",
  },
];

const slides = [
  {
    heading: "Клиенты о нас",
    content:
      "ООО «Вэбест» является нашим партнёром в сфере рекламной деятельности. За время сотрудничества ООО «Вэбест» подтвердила свой высочайший профессиональный статус, активность и компетентность в выполнении поставленных задач. Все задачи выполняются вовремя, в строго обозначенные сроки и с отличным качеством. Сотрудники компании качественно справляются со своими обязанностями. Мы довольны работами ООО «Вэбест» и готовы рекомендовать эту компанию как ответственного и надёжного партнёра.",
    src: "/images/imageMarketing9.png",
    username: "Игнатьев Станислав",
    occupation: "Директор по Маркетингу, Olymp men",
  },
  {
    heading: "Клиенты о нас",
    content:
      "ООО «Вэбест» является нашим партнёром в сфере рекламной деятельности. За время сотрудничества ООО «Вэбест» подтвердила свой высочайший профессиональный статус, активность и компетентность в выполнении поставленных задач. Все задачи выполняются вовремя, в строго обозначенные сроки и с отличным качеством. Сотрудники компании качественно справляются со своими обязанностями. Мы довольны работами ООО «Вэбест» и готовы рекомендовать эту компанию как ответственного и надёжного партнёра.",
    src: "/images/imageMarketing9.png",
    username: "Игнатьев Станислав",
    occupation: "Директор по Маркетингу, Olymp men",
  },
  {
    heading: "Клиенты о нас",
    content:
      "ООО «Вэбест» является нашим партнёром в сфере рекламной деятельности. За время сотрудничества ООО «Вэбест» подтвердила свой высочайший профессиональный статус, активность и компетентность в выполнении поставленных задач. Все задачи выполняются вовремя, в строго обозначенные сроки и с отличным качеством. Сотрудники компании качественно справляются со своими обязанностями. Мы довольны работами ООО «Вэбест» и готовы рекомендовать эту компанию как ответственного и надёжного партнёра.",
    src: "/images/imageMarketing9.png",
    username: "Игнатьев Станислав",
    occupation: "Директор по Маркетингу, Olymp men",
  },
  {
    heading: "Клиенты о нас",
    content:
      "ООО «Вэбест» является нашим партнёром в сфере рекламной деятельности. За время сотрудничества ООО «Вэбест» подтвердила свой высочайший профессиональный статус, активность и компетентность в выполнении поставленных задач. Все задачи выполняются вовремя, в строго обозначенные сроки и с отличным качеством. Сотрудники компании качественно справляются со своими обязанностями. Мы довольны работами ООО «Вэбест» и готовы рекомендовать эту компанию как ответственного и надёжного партнёра.",
    src: "/images/imageMarketing9.png",
    username: "Игнатьев Станислав",
    occupation: "Директор по Маркетингу, Olymp men",
  },
  {
    heading: "Клиенты о нас",
    content:
      "ООО «Вэбест» является нашим партнёром в сфере рекламной деятельности. За время сотрудничества ООО «Вэбест» подтвердила свой высочайший профессиональный статус, активность и компетентность в выполнении поставленных задач. Все задачи выполняются вовремя, в строго обозначенные сроки и с отличным качеством. Сотрудники компании качественно справляются со своими обязанностями. Мы довольны работами ООО «Вэбест» и готовы рекомендовать эту компанию как ответственного и надёжного партнёра.",
    src: "/images/imageMarketing9.png",
    username: "Игнатьев Станислав",
    occupation: "Директор по Маркетингу, Olymp men",
  },
];

const title = "Интернет-маркетинг";
const subtitle =
  "Доверьте нам маркетинг вашего бизнеса от медиа и performance-кампаний до полноценного brandformance";
const buttonTitle = "Оставить заявку";
const imageSrc = "/images/imageMarketing1.png";
const imageAlt = "Заголовок статьи";
const imageCaption = "";
</script>

<template>
  <div class="expertise-marketing">
    <ExpertiseHeading
      :breadcrumbItems="breadcrumbItems"
      :title="title"
      :subtitle="subtitle"
      :buttonTitle="buttonTitle"
      :imageSrc="imageSrc"
      :imageAlt="imageAlt"
      :imageCaption="imageCaption"
    />

    <Advantages :cards="cards" title="Наши компетенции" :forbidden="true" />

    <Priority :subtitle="false" title="Почему мы" :prioritys="priorityItems" />

    <BlogUnit title="Награды и сертификаты" article="development" />

    <Recruiting />

    <BlogUnit title="Наши кейсы" article="case" :slider="true" />

    <CustomersUnit />

    <div class="container">
      <ArticleSlider
        :slides="slides"
        :review="true"
        style="margin-bottom: 220px"
      />
    </div>

    <ArticleSliderMobile :slides="slides" :review="true" />

    <TalkUnit />
  </div>
</template>

<style lang="scss">
.expertise-marketing {
  display: flex;
  flex-direction: column;
  padding-top: var(--page-padding);

  .outstaff-advantages__list {
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr;
  }

  .outstaff-advantages__item-image {
    max-width: 350px;
  }
}
</style>
