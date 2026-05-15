<script setup>
import footerData from "@/data/footer_data.json";
</script>

<template>
  <table class="footer">
    <tr><td><div class="footer-separator"></div></td></tr>
    <tr>
      <td class="footer-content">
        <div class="footer-links">
          <a href="#">{{ footerData.contactUs }}</a> |
          <a href="#">{{ footerData.terms }}</a> |
          <a href="#">{{ footerData.corporate }}</a>
        </div>
        <div class="footer-copy">{{ footerData.copyright }}</div>
      </td>
    </tr>
  </table>
</template>
