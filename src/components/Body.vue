<template lang="html">
    <div>
      <!-- Tabs with card integration -->
      <b-card no-body>
        <b-tabs small card ref="tabs" class="mx-auto w-75 col-md-6 col-xs-12">
          <b-tab title="Personal Information">
            <user-info></user-info>
          </b-tab>
          <b-tab title="Learning Courses">
            <user-projects></user-projects>
          </b-tab>
          <b-tab title="Complete Courses">
            <user-schedule></user-schedule>
          </b-tab>
          <b-tab title="Notification">
            <about-us></about-us>
          </b-tab>
        </b-tabs>
      </b-card>
    </div>
</template>

<script>
import UserInfo from './UserInfo.vue';
import UserProjects from './UserProjects.vue';
import UserSchedule from './UserSchedule.vue';
import AboutUs from './AboutUs.vue'

export default {
  components:{
    'user-info': UserInfo,
    'user-projects': UserProjects,
    'user-schedule': UserSchedule,
    'about-us': AboutUs
  },
  data(){
    return{

    }
  },
  computed: {
    usersProfile(){
      return this.$store.state.usersProfile;
    }
  }
}
</script>

<style lang="css" scoped>
  div.card{
    background: linear-gradient(to left, #ece9e6, #ffffff)!important; 
  }
</style>
