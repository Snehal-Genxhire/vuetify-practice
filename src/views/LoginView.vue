<template>
  <v-card max-width="400" class="mx-auto mt-16" color="grey-lighten-3">
    <v-card-title class="text-center">Login</v-card-title>
    <v-divider class="ma-16 mt-0 mb-0"></v-divider>
    <v-form @submit.prevent="onSubmit">
      <v-card-text class="ma-3">
        <v-text-field
          class="ma-3"
          label="Email"
          prepend-icon="mdi-email"
          type="email"
          clearable
          v-model="email"
        ></v-text-field>
        <v-text-field
          class="ma-3"
          label="Password"
          prepend-icon="mdi-lock"
          type="password"
          clearable
          v-model="password"
        ></v-text-field>
      </v-card-text>
      <v-btn block color="green" variant="tonal" type="submit">Login</v-btn>
    </v-form>
  </v-card>
</template>

<script >
import { ref } from "vue";
import { reactive } from "vue";
export default {
  name: "LoginView",
  setup() {
    const email = ref("admin@demo.com");
    const password = ref("admin");

    const login = () => {
      axios
        .post("/auth/login", {
          email: email.value,
          password: password.value,
        })
        .then((r) => {
          const { accessToken, userData, userAbilities } = r.data;

          localStorage.setItem("userAbilities", JSON.stringify(userAbilities));
          ability.update(userAbilities);
          localStorage.setItem("userData", JSON.stringify(userData));
          localStorage.setItem("accessToken", JSON.stringify(accessToken));

          // Redirect to `to` query if exist or redirect to index route
          router.replace(route.query.to ? String(route.query.to) : "/");
        })
        .catch((e) => {
          const { errors: formErrors } = e.response.data;

          errors.value = formErrors;
          console.error(e.response.data);
        });
    };

    const onSubmit = () => {
      refVForm.value?.validate().then(({ valid: isValid }) => {
        if (isValid) login();
      });
    };
  },
};
</script>