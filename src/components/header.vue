<template>
  <header class="header">
            <div class="container">
                <div class="header-nav">
                    <ul>
                        <li>Магазин</li>
                        <li>Стиль</li>
                        <li>О нас</li>
                        <li>Истории</li>
                    </ul>
                </div>
                <div class="header-box">
                    <router-link to="/" class="header-logo" logo> <img src="../assets/images/logo.png" alt="logo"></router-link>
                      
                </div>
                <div class="header-controls">
                    <button class="btn-primary" @click="openModal">
                    <img src="../assets/images/icon/Group.svg" alt="user"></button>
                    <button class="btn-search">
                     <img src="../assets/images/icon/Group (1).svg" alt="search"></button>
                    <button class="btn-outline" id="cart-button">
                    <img src="../assets/images/icon/shoppinh-cart.png" alt="shopping-cart"></button>
                </div>
            </div>
        </header>
</template>

<script setup>
const emit = defineEmits (['toggleModal'])
const openModal = () => emit('toggleModal')
</script>


<style>
.header {
  min-height: 124px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;



}

.header-box {
  height: 100%;
  align-items: center;
  display: flex;



}


.header-controls {
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  max-height: 50px;

}

.header-nav {

  flex-shrink: 0;
  align-items: center;
  justify-content: space-around;

}

.header-nav ul {
  display: flex;
  align-items: center;
  justify-content: space-around;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 15px;
  flex-wrap: wrap;

}

.header-nav ul li {
  color: #56593D;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 25.2px;
  letter-spacing: 1.575px;
  text-transform: uppercase;
  margin: 0;
}


.btn {
  display: flex;
  outline: none;
  cursor: pointer;
  justify-content: center;
  align-items: center;
  width: 32px;
  height: 32px;
  flex-shrink: 0;

}

.btn-primary {
  align-items: center;
  cursor: pointer;
  width: 23px;
  height: 23px;
  flex-shrink: 0;
  margin: 0;
  padding: 0;
  border: none
}

.btn-primary img {
  width: 100%;
  align-items: center;
  background-color: #FFFFFF;
}

.btn-search {
  align-items: center;
  cursor: pointer;
  width: 23px;
  height: 23px;
  flex-shrink: 0;
  margin: 9px;
  padding: 0;
  border: none
}

.btn-search img {
  width: 100%;
  align-items: center;
  background-color: #FFFFFF;


}

.btn-outline {
  cursor: pointer;
  width: 23px;
  height: 23px;
  flex-shrink: 0;
  margin: 0;
  padding: 0;
  border: none
}

.btn-outline img {
  width: 100%;
  align-items: center;
  background-color: #FFFFFF;

}

.logo {
  max-width: 100px;
  align-items: center;

}

.logo img {
  width: 100%;
}
</style>