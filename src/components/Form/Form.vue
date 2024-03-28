<template>
  <b-container id="form-container" class="pb-4" fluid>
    <b-row class="justify-content-md-center mt-5 mb-5">
      <b-col cols="8">
        <b-form @submit="onSubmit">
          <b-container>
            <b-row>
              <b-col cols="6" class="mt-4">
                <b-form-group
                  id="input-group-1"
                  label="NAME:"
                  label-class="form-label"
                  label-for="input-1"
                >
                  <b-form-input
                    id="input-1"
                    v-model="form.name"
                    placeholder="Type now..."
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
              <b-col cols="6" class="mt-4">
                <b-form-group
                  id="input-group-2"
                  label="EMAIL:"
                  label-for="input-2"
                  label-class="form-label"
                >
                  <b-form-input
                    id="input-2"
                    v-model="form.email"
                    type="email"
                    placeholder="Enter your email address"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
              <b-col cols="6" class="mt-4">
                <b-form-group
                  id="input-group-3"
                  label="PHONE NUMBER:"
                  label-for="input-3"
                  label-class="form-label"
                >
                  <b-form-input
                    id="input-3"
                    v-model="form.phone"
                    type="number"
                    placeholder="Enter your phone number"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
              <b-col cols="6" class="mt-4">
                <b-form-group
                  id="input-group-4"
                  label="COUNTRY:"
                  label-for="input-4"
                  label-class="form-label"
                >
                  <b-form-select
                    id="input-4"
                    v-model="form.country"
                    :options="countrys"
                    required
                    placeholder="Enter your phone number"
                  ></b-form-select>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row>
              <b-col cols="12" class="mt-4">
                <b-form-group
                  id="input-group-5"
                  label="MESSAGE:"
                  label-for="input-5"
                  label-class="form-label"
                >
                  <b-form-textarea
                    id="input-5"
                    v-model="form.message"
                    placeholder="Type a text messa..."
                    rows="6"
                    max-rows="6"
                  ></b-form-textarea>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="justify-content-md-center mt-5">
              <b-col cols="2">
                <b-button type="submit" variant="warning"
                  >Send Message</b-button
                >
              </b-col>
            </b-row>
          </b-container>
        </b-form>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Vue from "vue";
export default {
  name: "FormComponent",
  components: {},
  data() {
    return {
      form: {
        email: "",
        name: "",
        country: null,
        phone: "",
        message: "",
      },
      countrys: [
        { value: "Colombia", text: "Colombia" },
        { value: "USA", text: "USA" },
        { value: "Mexico", text: "Mexico" },
        { value: "España", text: "España" },
        { value: null, text: "Please select an option" },
      ],
    };
  },
  methods: {
    sendData() {
      Vue.ajax({ url: "", method: "" });
    },
  },
};
</script>

<style scoped>
#form-container {
  background-color: #2f5190;
}

form {
  /deep/ .form-label {
    color: white !important;
    font-weight: bold !important;
    margin-bottom: 1em;
  }

  /deep/ .custom-select {
    display: block;
    width: 100%;
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: var(--bs-body-color);
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background-color: var(--bs-body-bg);
    background-clip: padding-box;
    border: var(--bs-border-width) solid var(--bs-border-color);
    border-radius: var(--bs-border-radius);
    transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
  }
}
</style>
