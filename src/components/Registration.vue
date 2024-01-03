<template>
  <div class="cart-modal__body-login">
                          <form class="form_auth_style">
                            <input type="email" name="email" v-model=" email" placeholder="Введите Ваш имейл" required >
                            <input type="password" name="password"  v-model="password" autocomplete="off" placeholder="Введите пароль"  required >
                            <button v-on:click="auth" class="form_auth_button" type="submit" name="submit"  >Войти</button>
                          </form> 
                    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'App',
    data () {
        return {
            API_URL:'http://localhost:5173/',
            user: null ,
            email: '',
            password: '',
            isLoading: false,
        }
    }, 
    methods: {
        async auth() {
            this.isLoading = true
            await axios
            post(
                `${this.API_URL}/auth/login`,
                { email: this.email, password: this.password },
                {
                    headers: { 'Content-Type':'application/json'},
                }
            )
            .then(({ data }) => {
                this.user = data.user
                this.isLoading = false
            })
   
        },
    }  
}
//  вариант с токеном:  name: "Sign in",
//     data() {
//         return {
//             email: "",
//             password: ""
//         };
//     },
//     methods: {
//         login(event) {
//             event.preventDefault();
//             this.axios
//             .post(`http://localhost:5173/api/auth/token`, {'email': this.email, 'password': this.password})
//             .then(response => {this.setLogined(response.data.token)})
//             .catch(err => {console.error(err)})
//         },
//         setLogined(token) {
//             console.log(token)
//         }
//     }
// } 


</script>

<style>
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