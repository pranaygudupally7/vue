<template>
  <div class="home">
  <nav>
    <router-link to="/"><span @click="openHomeView()">Home</span></router-link>
  </nav>
    <HomeBanner 
      v-if="homeView"
    />
    <DoctorsList 
      v-if="homeView"
      :doctorDetailsViewFunc = "openDoctorDetailsView"
      :doctorDataList = doctorsData
    />
    <DoctorDetails 
      v-if="doctorDetailsView"
      :doctorDataList = doctorsData
      :docid = docID-1
    />
    <FooterComponent />
  </div>
</template>
<style>
  nav{
    background-color: #f5f2f2;
    border-radius: 10px;
    border: 1px solid rgb(207, 206, 206);
    margin-bottom: 5px;
  }
</style>
<script>
import HomeBanner from '@/components/HomeBanner.vue';
import DoctorsList from '@/components/DoctorsList.vue';
import DoctorDetails from '@/components/DoctorDetails.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  data(){
    return {
      homeView : true,
      doctorDetailsView : false,
      doctorsData : [],
      docID : 0,
    }
  },
  mounted() {
  fetch('https://doctors-node.onrender.com/api')
        .then(response => response.json())
        .then(data => {
          console.log(data);
]          this.doctorsData = data;
          console.log(this.doctorsData)
        })
        .catch(error => console.error('Error fetching JSON data:', error));
  },
  name: 'HomeView',
  components: {
    HomeBanner,
    DoctorsList,
    DoctorDetails,
    FooterComponent
},
methods : {
  openDoctorDetailsView(id){
    this.homeView = false
    this.doctorDetailsView = true
    this.docID = id
  },
  openHomeView(){
    this.homeView = true
    this.doctorDetailsView = false
  }
}
}
</script>
