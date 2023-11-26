<template>
    <div>
      <Header />
      <div class="content-area">
        <div class="sidebox"></div> <!-- Left panel -->
        <div class="posts">
          <!-- Dynamic posts will be rendered here -->
        </div>
        <div class="sidebox"></div> <!-- Right panel -->
      </div>
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '@/components/CompoHeader.vue';
  import Footer from '@/components/CompoFooter.vue';
  
  export default {
    name: 'MainPage',
    components: {
      Header,
      Footer
    }
  };
  </script>
  
  <style scoped>
  .content-area {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
    padding: 0 20px;
    min-height: calc(100vh - 60px - 40px);
    gap: 20px;
  }
  
  .sidebox {
    background-color: #868686;
    width: 15%;
    flex-grow: 1;
    border-radius: 10px;
  }
  
  .posts {
    width: 68%;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  
  </style>
  