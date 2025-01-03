<template>
    <div class="loading">
      <h2>{{ title }}</h2>
      <div class="spinner"></div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: false,
        default: 'Loading...',
      },
    },
  };
  </script>
  
  <style scoped>
  .loading {
    text-align: center;
    margin-top: 50px;
  }
  .spinner {
    margin: 20px auto;
    width: 40px;
    height: 40px;
    border: 4px solid rgba(0, 0, 0, 0.2);
    border-top-color: #3498db;
    border-radius: 50%;
    animation: spin 1s linear infinite;
  }
  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  </style>
  