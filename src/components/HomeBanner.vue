<template>
    <div class="hero-background-image">
        <h1 class="main-title">Doc Check</h1>
        <div class="container">
            <div class="hero-text">
                <h1>
                    Find the doctor you like to take care of your health and wellbeing
                </h1>
                <p class="hero-description">
                    Easily browse through a curated list of experienced doctors, each with a detailed bio showcasing their expertise and background. Discover the perfect match for your needs by exploring their availability schedules, ensuring convenient appointment options. Empower yourself with informed healthcare choices as you navigate through our platform, connecting seamlessly with trusted medical professionals. Elevate your healthcare experience with our comprehensive site, designed to simplify doctor selection and enhance your journey to well-being
                </p>
            </div>
        </div>
    </div>
</template>

<style>
.main-title{
    font-size: 40px;
}
.container{
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-radius: 10px;
}

.hero-background-image{
    padding-top: 10px;
    background-image: url('../assets/images/doctors-hero-img.jpeg');
    background-size: cover;
}
.hero-image-image{
    height: 400px;
    width: 90%;
    padding: 30px;
    margin-right: 20px;
    border-radius: 20px;
}
.hero-image{
    border-radius: 20px;
}
.hero-text{
    height: 500px;
}
.hero-description{
    width: 500px; 
    text-align: justify; 
    margin: 30px;
}

@media (max-width: 768px) { 
    .container{
        display: grid;
        grid-template-columns: 1fr;
    }
    .hero-image-image{
    height: 200px;
    width: 80%;
    padding: 30px;
    margin-right: 30px;
    border-radius: 20px;
    }
    .hero-text{
        width: 300px;
        margin-left: 15px;
    }
    .hero-description{
        width: 250px; 
        text-align: justify; 
        margin: 30px;
    }
    .hero-background-image{
        height: 740px;
    }
}


</style>

<script>

export default {
    name: 'homebanner'
}
</script>