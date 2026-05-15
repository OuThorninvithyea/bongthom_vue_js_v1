<script setup>
import quickLinks from '@/data/quick_links_data.json'



</script>

<template>
  <table class="sb-table">
    <tr>
      <td class="sb-main-header">
        quick_link
      </td>
    </tr>
<tr>
    <td class="sb-pink-row quick-link-id-row">
      <div class="quick-link-id">
        Bong Thom-ID:
        <input type="text">
        <button type="button">&gt;</button>
      </div>
    </td>
    </tr>

    <tbody>
    <tr v-for="link in quickLinks" :key="link.text">
      <td class="sb-pink-row" :style="link.textAlgin ? { textAlign: link.textAlgin } : {}">
        <img v-if="link.facebookImg" src="@/assets/images/facebook.jpg" alt="Facebook Logo">
        <a href="#" :class="{ blue: link.style === 'blue' }">
          {{ link.text }}
        </a>
        <span v-if="link.badge" class="sb-badge-new">
          {{ link.badge }}
        </span>
      </td>
    </tr>
    </tbody>

  </table>
</template>

<style scoped>
.sb-pink-row {
  display: flex;
  align-items: center;
}

a {
  color: #333333;
  text-decoration: none;
}

a.blue {
  color: #0000ee;
}

</style>
