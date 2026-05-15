<script setup>
import otherAnnouncementsData from "@/data/other_announcements_data.json";
</script>

<template>
  <table>
  <tr v-for="link in otherAnnouncementsData" :key="link.text" :class="link.heading ? '' : 'sb-pink-row quicklist'">
    <td>
      <span href="#" v-if="link.heading" class="sb-sub-header">{{ link.text }}</span>
      <a href="#" v-else :class="link.style === 'blue' ? 'blue-link' : ''">
        {{ link.text }}
        <template v-if="link.count"> ({{ link.count }})</template>
      </a>
    </td>
  </tr>
  </table>
</template>

<style scoped>
.sb-sub-header {
  display: block;
  background-color: #e0e8f8;
  color: #0000ff;
  text-align: center;
  font-weight: bold;
}

a {
  font-weight: 400;
  color: #333333;
  text-decoration: none;
}

a.blue-link {
  color: #0000ff;
}

table {
  width: 100%;
}

.sb-pink-row.quicklist {
  display: flex;
  width: 100%;
}
</style>
