




















<script lang="ts" setup>
  let age: string = '43';
  // age = 231;

  console.log(age);
  

</script>

<template>

  <div class="container">

    <header>
      <span class="barsIcon">
        <font-awesome-icon :icon="['fas', 'bars']" />
      </span>
      <p class="title">Easy Shop</p>
      <span class="userIcon">
        <font-awesome-icon :icon="['far', 'user']" />
        <font-awesome-icon :icon="['far', 'heart']" />
        <font-awesome-icon :icon="['fas', 'cart-shopping']" />
      </span>
    </header>

    <body>

      <div class="latest">

      </div>

      <div class="information">
        <p class="informationPar">In our site you can buy and sell all kinds of entertainment products. From books to
          the latest VR sets.</p>
      </div>

      <div class="sections">

      </div>

    </body>

    <footer></footer>

  </div>

</template>

<style scoped>

.container {
  display: grid;
  grid-template-areas:
    "header"
    "body"
    "footer";
}

header {
  grid-area: header;
  display: flex;
  background-color: #413C58;
  height: 12vh;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  grid-area: body;
}

.latest {
  border: 2px solid black;
  border-radius: 3px;
  width: 90%;
  height: 300px;
  margin-top: 50px;
}

.information {
  display: flex;
  justify-content: center;
  width: 100%;
  height: 10vh;
  margin-top: 20px;
  background-color: #e9e8e8;
}

.informationPar {
  align-self: center;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: 1.1rem;
}

.sections {
  display: grid;
  grid-template-areas:
    "books gaming"
    "technology sport"
  ;
  width: 90%;
  height: 30vh;
  background-color: #e9e8e8;
  margin-top: 20px;
  margin-bottom: 20px;
  gap: 5px;
}

.title {
  align-self: center;
  font-size: 1.5rem;
  font-weight: bold;
  font-family: Georgia, "Times New Roman", Times, serif;
  color: white;
  margin-left: 20px;
}

.barsIcon {
  color: white;
  font-size: 1.5rem;
  align-self: center;
  margin-left: 20px;
}

.userIcon {
  color: white;
  align-self: center;
  margin-left: auto;
  margin-right: 20px;
  font-size: 1.5rem;
}

footer {
  background-color: #413C58;
  grid-area: footer;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 10vh;
  width: 100%;
  margin-top: 20px;
}
</style>
