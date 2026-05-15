<script setup>
  import rssFile from "@/data/rss_file_data.json";
  import cellcard from "@/assets/images/feed-icon.gif"
</script>

<template>
  <table>
    <tr  v-for="link in rssFile" :key="link.text" class="sb-pink-row other-services">
      <td>
        <img :src="cellcard" alt="cellcard" />
        <a href="#">{{ link.text }}</a>
      </td>
    </tr>
  </table>
</template>

<style scoped>

  table {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

 a , img {
   text-decoration: underline;
   padding-left: 5px;
 }
</style>