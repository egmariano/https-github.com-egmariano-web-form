<template>
  <form>
    <label>Email: </label>
    <!--two-way data binding: v-model -->
    <input type="email" required v-model="email">
    <label>Password: </label>
    <input type="password" required v-model="password">
    <label>Role:</label>
    <select v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
    </select>
  <div class="terms">
    <input type="checkbox" required v-model="terms">
    <label>Accept terms and conditions </label>
  </div>

  <div>
    <input type="checkbox" v-model="names" value="shaun">
    <label>Shaun</label>
  </div>
  <div>
    <input type="checkbox" v-model="names" value="edgar">
    <label>Edgar</label>
  </div>
    <div>
    <input type="checkbox" v-model="names" value="ron">
    <label>Ron</label>
  </div>

  </form>
<p>Names: {{names}}</p>
</template>

<script>
  export default {
    data() {
      return {
        email: '',
        password: '',
        role: 'designer',
        terms: true,
        names: []
      }
    }
  }
</script>

<style>
  form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  label{
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
  }
  input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 3px;
  }
</style>