<template>
    <div>
      <h2>Leitor de Cookies do Subdomínio</h2>
      <div>
        <h3>Cookies Compartilhados:</h3>
        <pre>{{ cookies }}</pre>
      </div>
      <button @click="readCookies">Ler Cookies</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        cookies: ''
      };
    },
    methods: {
      readCookies() {
        this.cookies = document.cookie;
      }
    },
    mounted() {
      this.readCookies();
    }
  };
  </script>
  
  <style scoped>
  /* Estilos opcionais */
  pre {
    margin-top: 10px;
    border: 1px solid #ccc;
    padding: 10px;
    background-color: #f4f4f4;
  }
  button {
    padding: 8px 15px;
    cursor: pointer;
  }
  </style>