<script setup>
import headerData from "@/data/site_header_data.json";
</script>

<template>
  <div class="site-header">
    <table>
      <tr>
        <th rowspan="2">
          <a href="#">
            <img :src="headerData.logo" :alt="headerData.logoAlt">
          </a>
        </th>
        <td class="green">{{ headerData.titleGreen }}</td>
        <td class="blue">{{ headerData.titleBlue }}</td>
      </tr>
      <tr>
        <td colspan="2" class="slogan">{{ headerData.slogan }}</td>
      </tr>
    </table>
  </div>
</template>

<style scoped>

</style>