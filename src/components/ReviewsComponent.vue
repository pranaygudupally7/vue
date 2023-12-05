<template>
    <div class="container">
        <div class="card1">
            <h3>Joshua</h3>
            <p>"Great doctor!They are top notch knowledgeable and caring. Highly recommend!"</p>
        </div>
        <div class="card1">
            <h3>Kayla</h3>
            <p>"Great doctor!They are top notch knowledgeable and caring. Highly recommend!"</p>
        </div>
    </div>
</template>

<script>

export default{
    name: 'reviewscomponent'
}

</script>


<style scoped>
  .container {
    width: 100%;
    background-color: #f4e9e1;
  }

  .card1 {
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 15px;
    margin: 10px 0;
    margin-right: 20px;
    background-color: #f4e9e1;
  }

  h3 {
    font-weight: bold;
    margin-bottom: 5px;
    color: rgb(157, 157, 253);
  }

  p {
    margin-top: 10px;
    line-height: 1.5;
  }
</style>
