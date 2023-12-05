<template>
    <h1>{{ doctorDataList[docid].name }}</h1>
    <div class="container">
        <div class="lef">
            <div class="image">
                <img src="../assets/images/ron.jpeg" alt="Card Image" class="card-image"
                    v-if="docid==0"
                >
                <img src="../assets/images/sophia.avif" alt="Card Image" class="card-image"
                    v-if="docid==1"
                >
                <img src="../assets/images/elijah.jpeg" alt="Card Image" class="card-image"
                    v-if="docid==2"
                >
                <img src="../assets/images/olivia.jpeg" alt="Card Image" class="card-image"
                    v-if="docid==3"
                >
                <img src="../assets/images/nathan.png" alt="Card Image" class="card-image"
                    v-if="docid==4"
                >
                <img src="../assets/images/ava.jpeg" alt="Card Image" class="card-image"
                    v-if="docid==5"
                >
            </div>
            <div class="doc-deets">
                <h3>Full Name : Dr. {{ doctorDataList[docid].name }}</h3>
                <h3>Speciality : {{ doctorDataList[docid].speciality }}</h3>
                <h3>Years of Experience : {{ doctorDataList[docid].experience }}</h3>
            </div>
            <div class="availability">
                <h3>Availability : {{ doctorDataList[docid].availability }}</h3>
                <h3>
                    Online : <span v-if="doctorDataList[docid].online==true">Yes</span> <span v-if="doctorDataList[docid].online==false">No</span>
                </h3>
            </div>
        </div>
        <div class="right">
            <div class="about">
                <p style="text-align: justify;">
                    {{doctorDataList[docid].about}}
                </p>
            </div>
            <div class="reviews">
                <ReviewsComponent />
            </div>
        </div>
    </div>
</template>
<style scoped>
.container {
  display: flex;
  width: 100%;
  background-color: #e3d5ca;
}

.lef {
  width: 40%;
  padding: 20px; 
  box-sizing: border-box; 
}

.right {
  width: 60%;
  padding: 20px; 
  box-sizing: border-box;
}

.image,
.socials,
.availability,
.about,
.reviews {
  margin-bottom: 20px; 
  
}
img {
  height: 340px; 
  background-color: #ccc; 
  width: 80%;
  border: 1px solid rgb(148, 148, 148);
  border-radius: 10px;
  margin: 10px;
}
.about{
    padding: 20px;
    justify-content: space-evenly;
    background-color: #f4e9e1;
    border-bottom: 20px;
}
.doc-deets
{
    text-align: left;
    border: 1px solid black;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
}
.availability{
    text-align: left;
    border: 1px solid black;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
}
@media (max-width: 600px) {
  .container {
    flex-direction: column;
    flex-wrap: nowrap; 
  } 
  .lef{
    width: 100%;
  }
  .right{
    width : 100%;
  }
  img {
  height: 340px; 
  background-color: #ccc;
  width: 100%;
  border: 1px solid rgb(148, 148, 148);
  border-radius: 10px;
}
}
</style>
<script>

import ReviewsComponent from './ReviewsComponent.vue';


export default{
    name : 'doctordetails',
    props : ['docid','doctorDataList'],
    components : {
    ReviewsComponent,
}
}
</script>