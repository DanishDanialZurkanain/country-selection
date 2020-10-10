<template>
  <div class="my-3">
    <div class="container">
      <div class="row justify-content-center">
        <b-form>
          <b-form-group>
            <b-form-select
              v-model="selectedCountry"
              :options="countries"
              value-field="name"
              text-field="name"
              required
            >
            </b-form-select>
          </b-form-group>
        </b-form>
      </div>
      <hr />
      <div v-if="selectedCountry != ''">
        <b-alert show dismissible
          >Your from <b>{{ selectedCountry }}</b></b-alert
        >
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      countries: [],
      selectedCountry: "",
    };
  },

  created() {
    this.loadAllCountries();
  },

  methods: {
    loadAllCountries() {
      axios
        .get("https://restcountries.eu/rest/v2/all")
        .then((res) => {
          this.countries = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style scoped>
</style>