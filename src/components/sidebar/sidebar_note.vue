<script setup>
import sidebarNote from "@/data/sidebar_note_data.json";
</script>

<template>
  <div class="sidebar-note">
    {{ sidebarNote.text }}
  </div>
</template>