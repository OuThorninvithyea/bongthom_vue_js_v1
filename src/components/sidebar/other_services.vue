<script setup>
import otherServices from "@/data/other_services_data.json";
</script>

<template>
  <table class="sb-table">
    <tr><td class="sb-main-header">Other services</td></tr>
    <tr v-for="service in otherServices" :key="service.text">
      <td class="sb-pink-row other-service-note">{{ service.text }}</td>
    </tr>
  </table>
</template>