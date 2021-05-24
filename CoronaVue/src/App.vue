<template>
    <router-view/>
</template>

<style lang="scss">
  :root {
    --split-left: #fae9b8;
    --split-right: #042242;
    --primary-color: #fff;
  }
  *{
    margin: 0;
    padding: 0;
  }
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    min-height: 100vh;
    font-family: Poppins, sans-serif;
    font-weight: bold;
    font-size: 1em;
    color: var(--primary-color);
  }
  img {
    max-width: 100%;
  }

</style>
