<template>

  <div class="cart-modal__overlay"  :class="{open: isOpen}" @click.self="closeModal()">
            <div class="cart-modal">
                <div class="cart-modal__exit" >
                    <span class="cart-modal__header--close" @click="closeModal()" >
                        <img src="../assets/images/modal/Group 1.png" alt="close">
                    </span>
                </div>
                <div class="cart-modal__header">
                    <img src="../assets/images/modal/logo.svg" alt="login">
                </div>
                <div class="cart-modal__body"> 
                    <Registration />
                    <!-- <div class="cart-modal__body-login">
                          <form class="form_auth_style">
                            <input type="email" name="email" placeholder="Введите Ваш имейл" required >
                            <input type="password" name="password"  placeholder="Введите пароль"  required >
                            <button  class="form_auth_button" type="submit" name="submit"  >Войти</button>
                          </form> 
                    </div>
                    
         -->
                </div>
            </div>
            
          </div>
</template>

<script setup>
import Registration from './Registration.vue'

const {isOpen} = defineProps({isOpen: Boolean});
const emit = defineEmits (['toggleModal']);
const closeModal = () => emit('toggleModal');

// const loginFunc = () => {


// window.addEventListener('DOMContentLoaded', () => {
//     const loginForm = document.querySelector('.form_auth_style');
//     loginForm.addEventListener('submit', (e) => {
//         e.preventDefault();
//         const fromData = new FormData(e.target);

//         for (var pair of fromData.entries()) {
//             console.log(pair[0] + ": " + pair[1]);
//         }
//     })
//     console.log(loginForm);
// })

// }

// loginFunc()

</script>

<style scoped>
.cart-modal__overlay {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(113, 115, 83, 0.38);
    display: none;
    align-items:center ;
    justify-content: center;

}
.cart-modal__overlay.open {
    display: flex;
}

.cart-modal {
    max-width: 678px;
    width: 100%;
    height: 418px;
flex-shrink: 0;
background-color: #FFFFEF;

}

.cart-modal__exit {
    display: flex;
    justify-content: end;
    margin-right: 15px;
    margin-top: 15px;
    cursor: pointer;
}
.cart-modal__header{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 30px;

}
.cart-modal__body-login{
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0px;
}
.form_auth_style{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 5px;
}

.form_auth_style input{
    margin: 5px;
    width: 250px;
height: 58px;
flex-shrink: 0;
background-color: #FFF;
border-radius: none;
color: rgba(86, 89, 61, 0.50);
font-family: Roboto;
text-align: center;
font-size: 12px;
font-style: normal;
font-weight: 400;
line-height: 25.2px; /* 157.5% */
letter-spacing: 1.575px;
text-transform: uppercase;
}
.form_auth_button {
    width: 100px;
height: 54px;
flex-shrink: 0;
background-color: #56593D;
color: #FFF;
font-family: Roboto;
margin: 20px;
cursor: pointer;
}


</style>