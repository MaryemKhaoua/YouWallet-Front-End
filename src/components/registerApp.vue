<template>
  <section class="">
    <div class="mask d-flex align-items-center h-100 gradient-custom-3">
      <div class="container h-100">
        <div class="row d-flex justify-content-center align-items-center h-100">
          <div class="col-12 col-md-9 col-lg-7 col-xl-6">
            <div class="card" style="border-radius: 15px;">
              <div class="card-body p-5">
                <h2 class="text-uppercase text-center mb-5">Create an account</h2>

                <form @submit.prevent="register">
                  <div class="form-outline mb-4">
                    <input v-model="name" type="text" id="form3Example1cg" class="form-control form-control-lg" />
                    <label class="form-label" for="form3Example1cg">Your Name</label>
                  </div>

                  <div class="form-outline mb-4">
                    <input v-model="email" type="email" id="form3Example3cg" class="form-control form-control-lg" />
                    <label class="form-label" for="form3Example3cg">Your Email</label>
                  </div>

                  <div class="form-outline mb-4">
                    <input v-model="password" type="password" id="form3Example4cg" class="form-control form-control-lg" />
                    <label class="form-label" for="form3Example4cg">Password</label>
                  </div>

                  <div class="d-flex justify-content-center">
                    <button type="submit" class="btn btn-success btn-block btn-lg gradient-custom-4 text-body">Register</button>
                  </div>

                  <p class="text-center text-muted mt-5 mb-0">Have already an account? <router-link to="/login">LogIn</router-link>.</p>
                </form>

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script>
import axios from 'axios';
export default {
  data() {
    return {
      name: '',
      email: '',
      password: '',
    };
  },
  methods: {
    async register() {
      try {
        const response = await axios.post('http://127.0.0.1:8000/api/register', {
          name: this.name,
          email: this.email,
          password: this.password,
        });

       console.log(response.data);
       this.$router.push('/login');

      } catch (error) {
        console.error('registration failed:', error);
      }
    },
  },
};
</script>

