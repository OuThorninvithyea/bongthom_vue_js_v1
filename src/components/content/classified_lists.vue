<script setup>
import newIcon from "@/assets/images/new.png";
import classifiedsTitles from "@/data/classified_data_title.json";
import classifiedsDetails from "@/data/classified_details_data.json";
</script>

<template>
  <table class="content-table">
    <tr class="content-row">
      <td class="qv-col classifieds-col">
        <div class="qv-header-class">
          Quick View Latest Classifieds
          <span class="qv-header-note">
          </span>
        </div>

        <div class="qv-search-row">
          Search Classifieds Title
          <input type="text">
          <button type="button">&gt;</button>
        </div>

        <div class="classifieds-wrap">
          <table class="qv-list" id="classifieds-list">
            <tbody>
            <tr v-for="(classified, index) in classifiedsTitles" :key="classified.title">
              <td>
                <div class="classified-wrapper">
                  <span class="dot">&#8226;</span>
                  <div class="title-wrapper">
                    <a href="#" class="classified-data-title">{{ classified.title }}</a>
                    <span v-if="classifiedsDetails[index]" class="qv-detail">{{ classifiedsDetails[index].detail }}</span>
                  </div>
                </div>
              </td>
            </tr>
            </tbody>
          </table>
        </div>

        <div class="qv-all-link-wrap">
          <a href="#" class="qv-all-link">Quick View all active classifieds</a>
        </div>
      </td>
    </tr>
  </table>
</template>

<style scoped>

.dot {
  color: #000;
}

.classified-wrapper {
  display: flex;
  gap: 5px;
  flex-direction: row;
}

.classified-wrapper > span {
  flex-shrink: 0;
}

.title-wrapper {
  display: flex;
  flex-direction: column;
}

</style>
