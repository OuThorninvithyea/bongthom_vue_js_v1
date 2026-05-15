<script setup>
import SiteHeader from "@/components/header/site_header.vue";
import LanguageBar from "@/components/header/language_bar.vue";
import SearchNav from "@/components/header/search_nav.vue";
import SiteSidebar from "@/components/sidebar/site_sidebar.vue";
import QuickView from "@/components/content/quick_view.vue";
import Classified_lists from "@/components/content/classified_lists.vue";
import SiteFooter from "@/components/footer/site_footer.vue";
</script>

<template>
  <div class="container">
    <SiteHeader />
    <LanguageBar />
    <SearchNav />
    <div class="main-layout">
      <SiteSidebar />
      <QuickView />
      <Classified_lists />
    </div>
    <SiteFooter />
  </div>
</template>
