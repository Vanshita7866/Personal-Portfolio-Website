<template>
  <div class="contact">
    <h2>Contact Me</h2>
    <form >
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="name" required />

      <label for="email">Email:</label>
      <input type="email" id="email" v-model="email" required />

      <label for="message">Message:</label>
      <textarea id="message" v-model="message" required></textarea>

      <button @click.prevent="submitForm">Submit</button>
    </form>

    <div v-if="submitted">
      <h3>Thank you for your message, {{ name }}!</h3>
      <p>Email: {{ email }}</p>
      <p>Message: {{ message }}</p>
    </div>

    <!-- Example of v-for -->
    <div v-if="submitted">
      <h3>Previous Messages:</h3>
      <ul>
        <li v-for="(msg, index) in previousMessages" :key="index">
          {{ msg }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      message: '',
      submitted: false,
      previousMessages: [], // Example data for v-for
    };
  },
  methods: {
    submitForm() {
      // Simulate form submission logic
      // In a real application, you would send the form data to a server
      this.submitted = true;
      this.previousMessages.push(this.message); // Adding message to previous messages
    },
  },
};
</script>
<style scoped>
  input[type=text], select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type=submit] {
  width: 100%;
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #45a049;
}

div {
  border-radius: 5px;
  background-color: #b79a81;
  padding: 20px;
  margin: 10px;
}

form ,h2{
  color: #ffffff;
}
  </style>
