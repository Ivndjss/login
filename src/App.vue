<template>
    <v-app>
      <v-content>
        <v-container fluid>
          <v-row align="center" justify="center">
            <v-col cols="12" sm="8" md="6" lg="4">
              <v-card class="auth-inner">
                <v-card-title>
                  <h3>Login</h3>
                </v-card-title>
                <v-card-text>
                  <v-form @submit.prevent="login">
                    <v-text-field
                      v-model="loginData.email"
                      label="Email"
                      type="email"
                      required
                    ></v-text-field>
                    <v-text-field
                      v-model="loginData.password"
                      label="Password"
                      type="password"
                      required
                    ></v-text-field>
                    <v-btn type="submit" color="primary" block>Login</v-btn>
                  </v-form>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
          <v-row align="center" justify="center" class="mt-4">
            <v-col cols="12" sm="8" md="6" lg="4">
              <v-card class="auth-inner">
                <v-card-title>
                  <h3>Registration</h3>
                </v-card-title>
                <v-card-text>
                  <v-form @submit.prevent="register">
                    <v-text-field
                      v-model="registerData.name"
                      label="Name"
                      required
                    ></v-text-field>
                    <v-text-field
                      v-model="registerData.email"
                      label="Email"
                      type="email"
                      required
                    ></v-text-field>
                    <v-text-field
                      v-model="registerData.password"
                      label="Password"
                      type="password"
                      required
                    ></v-text-field>
                    <v-btn type="submit" color="primary" block>Register</v-btn>
                  </v-form>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-content>
    </v-app>
  </template>
  
  <script>
  export default {
    data() {
      return {
        loginData: {
          email: "",
          password: "",
        },
        registerData: {
          name: "",
          email: "",
          password: "",
        },
      };
    },
    methods: {
      login() {
        // Perform login logic using this.loginData.email and this.loginData.password
        console.log("Login:", this.loginData);
        // Clear login form after submission
        this.loginData.email = "";
        this.loginData.password = "";
      },
      register() {
        // Perform registration logic using this.registerData.name, this.registerData.email, and this.registerData.password
        console.log("Registration:", this.registerData);
        // Clear registration form after submission
        this.registerData.name = "";
        this.registerData.email = "";
        this.registerData.password = "";
      },
    },
  };
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Fira+Sans:400,500,600,700,800');

    * {
        box-sizing: border-box;
    }

    body {
        background: #1C8EF9 !important;
        min-height: 100vh;
        display: flex;
        font-weight: 400;
        font-family: 'Fira Sans', sans-serif;
    }

    h1, h2, h3, h4, h5, h6, label, span {
        font-weight: 500;
        font-family: 'Fira Sans', sans-serif;
    }

    body, html, #app, #root, .auth-wrapper {
        width: 100%;
        height: 100%;
    }

    #app {
        text-align: center;
    }

    .navbar-light {
        background-color: #ffffff;
        box-shadow: 0px 14px 80px rgba(34, 35, 58, 0.2);
    }

    .auth-wrapper {
        display: flex;
        justify-content: center;
        flex-direction: column;
        text-align: left;
    }

    .auth-inner {
        width: 450px;
        margin: auto;
        background: #ffffff;
        box-shadow: 0px 14px 80px rgba(34, 35, 58, 0.2);
        padding: 40px, 55px, 45px, 55px;
        border-radius: 15px;
        transition: all .3s;
    }

    .auth-wrapper .form-control:focus {
        border-color: #167bff;
        box-shadow: none;
    }

    .auth-wrapper h3 {
        text-align: center;
        margin: 0;
        line-height: 1;
        padding-bottom: 20px;
    }

    .custome-control-label {
        font-weight: 400;
    }

    .forgot-password,
    .forgot-password a {
        text-align: right;
        font-size: 13px;
        padding-top: 10px;
        color: #7f7d7d;
        margin: 0;
    }
        
    .forgot-password a {
        color: #167bff;
    }

</style>

