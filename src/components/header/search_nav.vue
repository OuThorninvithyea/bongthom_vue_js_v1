<script setup>
import searchNavData from "@/data/search_nav_data.json";
</script>

<template>
  <table class="search-nav-table">
    <tr>
      <td class="search-block jobs-search">
        <ul class="auth-links-nav">
          <li v-for="link in searchNavData.authLinks" :key="link.text">
            <img :src="link.icon" alt="">
            <a href="#">{{ link.text }}</a>
          </li>
        </ul>
      </td>

      <td
        v-for="item in searchNavData.navItems" :key="item.text" class="search-block classifieds-search">
        <div class="nav-item-content">
          <img :src="item.icon" :alt="item.text">
          <span :class="['text-col', item.padClass]">{{ item.text }}</span>
        </div>
      </td>
    </tr>
  </table>
  <img src="@/assets/images/secure.gif" width="13" alt="Secure">
</template>