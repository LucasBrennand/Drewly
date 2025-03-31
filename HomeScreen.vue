<template>
    <div class="home-screen">
      <h1 class="title">Drooly!</h1>
      <h2 class="subtitle">Let's Draw!</h2>
      <button class="start-button" @click="startGame">Start Drawing!</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomeScreen',
    methods: {
      startGame() {
        // Emit an event or route to the drawing screen
        this.$emit('start-game');
        // Alternatively, use Vue Router:
        // this.$router.push('/draw');
      }
    }
  }
  </script>
  
  <style scoped>
  .home-screen {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #FFD166; /* Bright yellow background */
    font-family: 'Comic Sans MS', cursive, sans-serif; /* Kid-friendly font */
    text-align: center;
  }
  
  .title {
    font-size: 4rem;
    color: #EF476F; /* Pink/red color */
    margin: 0;
    text-shadow: 3px 3px 0 #06D6A0; /* Fun shadow effect */
    animation: bounce 1s infinite alternate;
  }
  
  .subtitle {
    font-size: 2.5rem;
    color: #118AB2; /* Blue color */
    margin: 20px 0 40px;
  }
  
  .start-button {
    padding: 15px 30px;
    font-size: 1.5rem;
    background-color: #06D6A0; /* Green color */
    color: white;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: transform 0.2s, background-color 0.2s;
  }
  
  .start-button:hover {
    transform: scale(1.05);
    background-color: #EF476F; /* Pink/red on hover */
  }
  
  @keyframes bounce {
    from {
      transform: translateY(0);
    }
    to {
      transform: translateY(-20px);
    }
  }
  </style>