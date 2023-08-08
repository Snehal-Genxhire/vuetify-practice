<template>
  <h2 class="text-center">Form</h2>
  <v-card
    max-width="800"
    color="grey-lighten-3"
    class="mx-auto ma-16"
    :loading="loading"
  >
    <v-card-text>User Form</v-card-text>
    <v-form @submit.prevent v-model="form">
      <v-container>
        <v-row>
          <v-col cols="6">
            <v-text-field
              v-model="firstName"
              label="First Name"
              required
              :counter="10"
              clearable
              :rules="nameRule"
              prepend-icon="mdi-account"
            >
            </v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field
              label="Last Name"
              :counter="10"
              required
              clearable
              v-model="lastName"
              :rules="nameRule"
              prepend-icon="mdi-account"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="6">
            <v-text-field
              v-model="email"
              label="Email"
              required
              type="email"
              prepend-icon="mdi-email"
              :counter="20"
              clearable
              :rules="emailRule"
            >
            </v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field
              label="Mobile no"
              :counter="10"
              required
              prepend-icon="mdi-phone"
              type="number"
              clearable
              v-model="phoneNo"
              :rules="phoneRule"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="6">
            <v-autocomplete
              :items="['Reading', 'Dancing', 'Listening music', 'Swimming']"
              label="Interests"
              multiple
              prepend-icon="mdi-heart"
              chips
              clearable
            ></v-autocomplete>
          </v-col>
          <v-col cols="6">
            <v-autocomplete
              :items="['Fresher', 'Experienced']"
              label="Work Experience"
              :rules="workRule"
              prepend-icon="mdi-briefcase"
              clearable
            ></v-autocomplete>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="6">
            <v-radio-group
              label="Gender"
              v-model="inline"
              inline
              :rules="genderRule"
            >
              <v-radio label="Male" value="male"></v-radio>
              <v-radio label="Female" value="female"></v-radio>
            </v-radio-group>
          </v-col>
          <v-col cols="6"> </v-col>
        </v-row>
        <v-checkbox v-model="checkbox" :rules="checkboxRule" color="green" label="Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit, placeat adipisci necessitatibus mollitia reprehenderit consequatur!"></v-checkbox>
        <v-btn type="submit" @click="submit">Submit</v-btn>
      </v-container>
    </v-form>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      loading: false,
      form: "",
      inline: null,
      firstName: null,
      lastName: null,
      email: null,
      phoneNo: null,
      checkbox:false,
      nameRule: [
        (v) => !!v || "Name is required",
        (v) =>
          (v && v.length >= 4) || "Name must be greater than 4 character  ",
      ],
      emailRule: [
        (v) => !!v || "Email is required",
        (value) => {
          if (/.+@.+\..+/.test(value)) return true;

          return "E-mail must be valid.";
        },
      ],
      phoneRule: [
        (v) => !!v || "Mobile number is required",
        (v) => {
          if (v.length > 10) return "Mobile number shoul be 10 digit";
          if (v.length < 10) return "Mobile number shoul be 10 digit";
        },
      ],
      genderRule: [(v) => !!v || " Please select gender"],
      workRule: [(v) => !!v || " Please Select Work experience"],
      checkboxRule:[(v) => !!v || " Please Select checkbox"]
    };
  },
  methods: {
    submit() {
      if (!this.form) return true;
      this.loading = true;
    },
  },
};
</script>