<script setup>
import jobTitles from "@/data/job_data_title.json";
import newIcon from "@/assets/images/new.png";
import newPink from "@/assets/images/newpink.png";
import companyData from "@/data/job_data_company.json";
import companyImage from "@/assets/images/company_img.png";

</script>

<template>
  <table class="content-table">
    <tr class="content-row">
      <td class="qv-col qv-divider jobs-col">
        <div class="qv-header-jobs">
          Quick View Latest Jobs
          <span class="qv-header-note">
            <img :src="newIcon" alt="newIcon">
          </span>
        </div>

        <div class="qv-search-row">
          Search Job Title
          <input type="text">
          <button type="button">&gt;</button>
        </div>

        <div class="job-title-wrap">
          <table class="qv-list jobs-list">
            <tbody>
              <tr v-for="(job, arrayIndex) in jobTitles" :key="job.title">
                <td>
                  <div class="job-wrapper">
                    <span class="dot">&#8226;</span>
                    <span v-if="job.isNew">
                      <img :src="newPink" alt="New" class="new-icon-pink">
                    </span>
                    <span v-else>
                      <img :src="newIcon" alt="Icon" class="new-icon-blue">
                    </span>
                    <div class="title-wrapper">
                    <a href="#" class="title-text">{{ job.title }}</a>
                      <tr>
                        <td class="company-info">
                    <a v-if="companyData[arrayIndex]" href="#" class="job-company">{{ companyData[arrayIndex].company }}</a>
                      <span> <img :src="companyImage" alt=""></span>
                        </td>
                      </tr>
                    </div>
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="qv-all-link-wrap">
          <a href="#" class="qv-all-link">Quick View all active jobs</a>
        </div>
      </td>
    </tr>
  </table>
</template>

<style scoped>

.company-info {
  display: flex;
  flex-direction: row;
}


.dot {
  color: #000;
}

.title-wrapper {
  display: flex;
  flex-direction: column;
}

.job-wrapper {
  display: flex;
  gap: 5px;
  flex-direction: row;
}

.job-wrapper .new-icon-pink,
.job-wrapper .new-icon-blue {
  height: 16px;
  min-width: 16px;
}

.job-wrapper > span {
  flex-shrink: 0;
}

.job-wrapper .dot {
  flex-shrink: 0;
}

.job-company {
  text-decoration: none;
}

</style>