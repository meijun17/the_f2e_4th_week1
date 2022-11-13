<template>
  <FrontPage></FrontPage>
  <DialogBox></DialogBox>
  <IntroBanner></IntroBanner>
  <ThemeView></ThemeView>
  <EventIllistrate></EventIllistrate>
  <AwardView></AwardView>
  <QuestionView></QuestionView>
  <SponsorsView></SponsorsView>
  <FooterView></FooterView>
</template>

<script>
import FrontPage from "./views/FrontPage.vue";
import DialogBox from "./views/DialogBox.vue";
import IntroBanner from "./views/IntroBanner.vue";
import ThemeView from "./views/ThemeView.vue";
import EventIllistrate from "./views/EventIllistrate.vue";
import AwardView from "./views/AwardView.vue";
import QuestionView from "./views/QuestionView.vue";
import SponsorsView from "./views/SponsorsView.vue";
import FooterView from "./views/FooterView.vue";

export default {
  name: "App",
  components: {
    FrontPage,
    DialogBox,
    IntroBanner,
    ThemeView,
    EventIllistrate,
    AwardView,
    QuestionView,
    SponsorsView,
    FooterView,
  },
};
</script>

<style lang="scss"></style>
