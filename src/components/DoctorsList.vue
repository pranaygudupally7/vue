<template>
    <div style="margin-top: 40px;">
        <h1>Choose from the doctors list</h1>
    </div>
    <div class="doctors-list-1">
      <div class="card"
      v-for="(doc,id) in doctorDataList.slice(0,3)"
      @click="doctorDetailsViewFunc(doc.id)"
      >
            <img src="../assets/images/ron.jpeg" alt="Card Image" class="card-image"
                v-if="id==0"
            >
            <img src="../assets/images/sophia.avif" alt="Card Image" class="card-image"
                v-if="id==1"
            >
            <img src="../assets/images/elijah.jpeg" alt="Card Image" class="card-image"
                v-if="id==2"
            >
            <div class="overlay">
            <h3>{{ doc.name }}</h3>
            <p>{{ doc.speciality }}</p>
            </div>
      </div>
    </div>
    <div class="doctors-list-2" style="margin-bottom: 40px; margin-top: 30px;">
        <div class="card"
             v-for="doc in doctorDataList.slice(3,6)"
             @click="doctorDetailsViewFunc(doc.id)"
            >
            <img src="../assets/images/olivia.jpeg" alt="Card Image" class="card-image"
                v-if="doc.id==4"
            >
            <img src="../assets/images/nathan.png" alt="Card Image" class="card-image"
                v-if="doc.id==5"
            >
            <img src="../assets/images/ava.jpeg" alt="Card Image" class="card-image"
                v-if="doc.id==6"
            >
            <div class="overlay">
            <h3>{{ doc.name }}</h3>
            <p>{{ doc.speciality }}</p>
            </div>
      </div>
    </div>
  </template>
  
  <style>
  .doctors-list-1{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 30px
  }


  .doctors-list-2 {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 30px
  }
  
  .card {
    width: calc(33.33% - 20px);
    margin-bottom: 20px;
    height: 400px;
    box-sizing: border-box;
    position: relative;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .card-image {
    width: 100%;
    height: auto;
    display: block;
    height: 300px;

  }

  img{
    height: 400px;
  }
  
  @media (max-width: 768px) {
  .card {
    width: calc(50% - 20px);  
  }
}

@media (max-width: 480px) {
  .card {
    width: 100%;
  }
}
  </style>
  
  <script>
  export default {
    name: 'doctorslist',
    props : ['doctorDetailsViewFunc','doctorDataList']
  }
  </script>
  