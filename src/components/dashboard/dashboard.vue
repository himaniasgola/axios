<template>
  <div id="dashboard">
    <h1>That's the dashboard!</h1>
    <p>You should only get here if you're authenticated!</p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  created() {
    axios.get('https://axiosproject-38470.firebaseio.com/users.json')
    .then(res => console.log(res))
    .catch(res => console.log(error))
  }
}
</script>
<style scoped>
  h1, p {
    text-align: center;
  }

  p {
    color: red;
  }
</style>