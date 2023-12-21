<script setup>
import MainLayout from '../components/MainLayout.vue';

// Page Title of Views
const pageTitle = 'About'
</script>

<template>
  <MainLayout :pageTitle="pageTitle">
    <section class="py-8 px-4 lg:py-12 lg:px-8">
      <div class="max-w-5xl mx-auto flex items-center justify-center flex-col lg:flex-row">
        <div class="mb-6 lg:mb-0 lg:mr-8">
          <!-- <img :src="profileImage" alt="Your Name" class="w-60 h-60 lg:w-150 lg:h-48 rounded-full object-cover shadow-md border-4 border-white"> -->
        </div>
        <div class="bg-white rounded-lg shadow-md p-6 text-gray-800">
          <h2 class="text-3xl lg:text-4xl font-bold mb-6">About Me</h2>
            <p class="text-lg lg:text-xl leading-relaxed mb-4 lg:mb-6 p-4">
              Hi there! My name is Cliyent V. Siclot. I'm 22 years old and currently reside in Cordova, Cebu, Philippines. I'm a fourth-year BSIT student pursuing a career as a front-end web developer or software engineer.
              <!-- Your description goes here -->
            </p>
            <p class="text-lg lg:text-xl leading-relaxed mb-4 lg:mb-6 p-4">
              I am a passionate individual who loves diving deep into various technologies. With a keen interest in software development and a strong background in...
              <!-- Your description goes here -->
            </p> 
            <!-- <p class="text-lg lg:text-xl leading-relaxed mb-4 lg:mb-6 p-4">
                Hello there! I am Your Name, a passionate and dedicated Bachelor of Science in Information Technology (BSIT) student. Technology has always fascinated me since I was young, igniting a curiosity that led me to pursue this dynamic field.
              
            </p>      -->
            <img :src="profileImage" alt="Your Name" class="w-60 h-60 lg:w-150 lg:h-48 rounded-full object-cover shadow-md border-4 border-white">       
        </div>
      </div>
    </section>
  </MainLayout>
</template>

<script>
export default {
  data() {
    return {
      pageTitle: "About Me",
      profileImage: require("../images/aboutimage.jpg") // Update with your image path
    };
  }
};
</script>



