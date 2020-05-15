<template>
  <div class="container">
    <h1>Users</h1>
    <hr>
    <table>
      <tr v-for="user in users" :key="user.id">
        <td>[ID] {{ user.id }}</td>
        <td>[Name] {{ user.name }}</td>
        <td>[Email] {{ user.email }}</td>
        <td>[Company Name] {{ user.company.name }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
const axios = require('axios').default;

const url = 'https://jsonplaceholder.typicode.com/users'
// const url = 'https://jsonplaceholder.typicode.com/users_for404test'

export default {
  asyncData({ params, error }) {
    return axios.get(url)
    .then((res) => {
      return { users: res.data }
    })
    .catch((e => {
      // console.log(e.response.status)
      // error({ users: e.response.status, message: e.message })
      error({ users: e.response.status, message: "404 error." })
    }))
  }
}
</script>
