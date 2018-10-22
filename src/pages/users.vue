<template>
  <Layout>
    <h1>Users list</h1>
    <dl v-for="user in $page.users.data">
      <dh>{{user.id}}</dh>
      <dd>{{user.name}}</dd>
    </dl>
  </Layout>
</template>

<page-query>
query Users {
  users(count: 10){
    data {
      name
      id
    }
  }
}
</page-query>

