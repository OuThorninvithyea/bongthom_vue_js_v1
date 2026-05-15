<script setup>
import QuickLink from '@/components/sidebar/quick_link.vue'
import SpecialSchedule from "@/components/sidebar/special_schedule.vue";
import OrganizationType from "@/components/sidebar/organization_type.vue";
import OtherAnnouncements from "@/components/sidebar/other_announcements.vue";
import Rss_file from "@/components/sidebar/rss_file.vue";
import OtherServices from "@/components/sidebar/other_services.vue";
import SidebarNote from "@/components/sidebar/sidebar_note.vue";
</script>

<template>
  <div class="sidebar">
    <QuickLink />
    <table class="sb-table">
      <tr><td class="sb-main-header">job Quick lists</td></tr>
      <tbody>
        <SpecialSchedule />
        <OrganizationType />
        <OtherAnnouncements />
      </tbody>
    </table>

    <OtherServices />

    <div class="site-lock-img">
      <img src="@/assets/images/sitelock_shield.png" alt="SiteLock Secure">
    </div>

    <table class="sb-table rss-table">
      <tr><td class="sb-main-header">RSS Files</td></tr>
    </table>

    <div class="rss-feeds-wrapper">
      <rss_file/>
    </div>

    <table class="sb-table">
      <tr class="sb-pink-row">
        <td class="rss-download">
          <span class="rss-footer">Click here</span>
          to download an RSS browser
        </td>
      </tr>
    </table>

    <SidebarNote />
  </div>
</template>
