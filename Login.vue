<template>
    <v-app>
      <v-main>
        <v-container fluid>
          <v-row align="center" justify="center">
            <v-col cols="12" sm="8" md="6" lg="4">
              <v-card class="login-card">
                <v-card-title class="login-title">
                  <h3>Login</h3>
                </v-card-title>
                <v-card-text>
                  <v-form @submit.prevent="login">
                    <v-text-field
                      v-model="loginData.email"
                      label="Email"
                      outlined
                      required
                    ></v-text-field>
                    <v-text-field
                      v-model="loginData.password"
                      label="Password"
                      type="password"
                      outlined
                      required
                    ></v-text-field>
                    <v-btn type="submit" color="primary" block>Login</v-btn>
                  </v-form>
                </v-card-text>
                <v-card-actions>
                  <div class="forgot-password">
                    <router-link to="/forgot-password">Forgot password?</router-link>
                  </div>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-main>
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
    },
  };
  </script>
  
  <style scoped>
  .login-card {
    margin-top: 100px;
  }
  
  .login-title {
    text-align: center;
  }
  
  .forgot-password {
    text-align: right;
    margin-top: 16px;
  }
  </style>
  