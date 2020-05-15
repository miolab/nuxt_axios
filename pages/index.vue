<template>
  <div class="container">
    <!-- <p>{{ users[0].id }}, {{ users[0].name }}</p> -->
    <ul>
      <li v-for="user in users" :key="user.id">
        [ID] {{ user.id }}, [Name] {{ user.name }}, [Email] {{ user.email }}, [Company Name] {{ user.company.name }}
      </li>
    </ul>
  </div>
</template>

<script>
const axios = require('axios').default;

// let url = 'https://jsonplaceholder.typicode.com/users'
let url = 'https://jsonplaceholder.typicode.com/users_hogehoge'

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
