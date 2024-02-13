<template>
  <form @submit.prevent="handleSubmit">
    <label>Title</label>
    <input type="text" v-model="title" required />
    <label>Details</label>
    <textarea v-model="details" required></textarea>
    <button>Add Project</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      details: '',
    };
  },
  methods: {
    handleSubmit() {
      let project = {
        title: this.title,
        details: this.details,
        complete: false,
        id: Math.floor(Math.random() * 10000),
      };
      console.log(project);

      fetch('http://localhost:3000/projects', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(project),
      })
        .then(() => {
          this.$router.push('/');
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style>
form {
  padding: 20px;
  border-radius: 10px;
  background: white;
}
label {
  display: block;
  margin: 20px 0 10px 0;
  color: #bbb;
  font-weight: bold;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 1px;
}
input {
  box-sizing: border-box;
  width: 100%;
  padding: 10px;
  border: 0;
  border-bottom: 1px solid #ddd;
}
textarea {
  box-sizing: border-box;
  width: 100%;
  height: 100px;
  padding: 10px;
  border: 1px solid #ddd;
}
form button {
  display: block;
  margin: 20px auto 0;
  padding: 10px;
  border: 0;
  border-radius: 6px;
  color: white;
  font-size: 16px;
  background: #00ce89;
}
</style>
