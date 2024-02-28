<template>
    <main>
    
   
    <div class="image">
      Movie
      <div class="grid grid-col-4 gap-5">
        <div v-for="p in shows" :key="p.id">
          
        </div>
    
      </div>
      </div>


</main>
    </template>
    <script setup>
   import { ref } from 'vue';

const searchInput = ref('');
const recipes = ref([]);


const searchRecipes = async () => {
 const apiKey = '90db8db9b008412b8b40259b66562850';
 const ingredient = searchInput.value;
 const url = `https://api.spoonacular.com/recipes/complexSearch?apiKey=${apiKey}&number=16&includeIngredients=${ingredient}`;


 try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    const data = await response.json();
    recipes.value = data.results;
 } catch (error) {
    console.error('Failed to fetch recipes:', error);
 }
};
    </script>
    
    <style>
.image{
background-image: url('https://img.freepik.com/free-photo/movie-background-collage_23-2149876028.jpg');
height:100vh;
background-size: cover;
text-align:center;
font-size:40px;
color:white;
}
</style>