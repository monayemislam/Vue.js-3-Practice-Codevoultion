<template>
  <div>
    <p>{{ JSON.stringify(formValues, null, 2) }}</p>
  </div>
  <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary"></textarea>
    </div>
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a Country</option>
        <option value="Bangladesh">Bangladesh</option>
        <option value="India">India</option>
        <option value="Pakistan">Pakistan</option>
        <option value="Singapore">Singapore</option>
      </select>
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="Bangladesh">Bangladesh</option>
        <option value="India">India</option>
        <option value="Pakistan">Pakistan</option>
        <option value="Singapore">Singapore</option>
      </select>
    </div>
    <div>
      <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
      <label for="remoteWork">Open to remote Work?</label>
    </div>
    <div>
      <label>Skill Set</label>
      <input
        type="checkbox"
        value="html"
        id="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        value="CSS"
        id="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        value="JavaScript"
        id="javascript"
        v-model="formValues.skillSet"
      />
      <label for="javascript">JavaScript</label>
    </div>
    <div>
      <label>Years of Experience</label>
      <input
        type="radio"
        value="0-2"
        id="0-2"
        v-model="formValues.yearsOfExperience"
      />
      <label for="0-2">0-2</label>
      <input
        type="radio"
        value="3-5"
        id="3-5"
        v-model="formValues.yearsOfExperience"
      />
      <label for="3-5">3-5</label>
      <input
        type="radio"
        value="6-10"
        id="6-10"
        v-model="formValues.yearsOfExperience"
      />
      <label for="6-10">6-10</label>
    </div>
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: false,
        skillSet: [],
        yearsOfExperience: "",
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log("Form Values", this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
label {
  font-weight: bold;
  display: flex;
  margin-right: 20px;
  margin-top: 10px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.43;
  color: #555;
  background-color: #fff;
  margin-top: 5px;
  background-image: none;
}
</style>
