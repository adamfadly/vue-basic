<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
    <AllFriends :friends="friends" @delete="deleteFriend"/>
    <OnlineFriends :friends="friends" />
    <Address :alamats="alamats" />
  </div>
</template>

<script>
import Navbar from './Navbar'
import AllFriends from './AllFriends'
import OnlineFriends from './OnlineFriends'
import Address from './Address'



export default {
  name: 'app',
  components: {
    Navbar,
    AllFriends,
    OnlineFriends,
    Address
  },

  data () {
    return {
     title: 'I will succes in software Development',
     friends: [
        { name: 'Mario', online: true },
        { name: 'Luigi', online: false },
        { name: 'Tood', online: true },
        { name: 'Bowser', online: false }
      ],
      alamats: [
        {name: 'budi', alamat: 'jl. saleh'},
        {name: 'joko', alamat: 'jl. nabi'},
        {name: 'may', alamat: 'jl. binus'},
        {name: 'dewo', alamat: 'jl. kemang'}
      ]
    }
  },
  methods: {
    deleteFriend(payload) {
      console.log(payload)
      this.friends = this.friends.filter( friend => {
        return friend.name !== payload.name
      })
    }
  }
}
</script>

<style>
#app{
  padding: 100px 200px;
}
h1 {
  color: #444;
  font-weight: normal;
  text-align: center;
}
</style>
