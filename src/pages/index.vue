<script>
import Sidebar from '../components/Sidebar.vue'
import MainNavbar from '../components/MainNavbar.vue'
import CandySectionList from '../components/CandySectionList.vue'
export default {
  components: {
    Sidebar,
    MainNavbar,
    CandySectionList,
  },
}
</script>
<template>
  <MainNavbar />
  <section class="flex">
    <div class="flex flex-col w-64 h-screen px-4 py-8 bg-white border-r">
      <Sidebar />
    </div>
    <div class="flex mx-auto">
      <CandySectionList />
    </div>
  </section>
</template>
