<template>
  <form @submit.prevent="subscribe">
    <input v-model="email" type="email" name="EMAIL" value="" autocapitalize="off" autocorrect="off" placeholder="Email Address" required>
    <input class="button" type="submit" value="Subscribe">
  </form>
</template>

<script>
  import axios from 'axios'

  export default {
    name: 'MailchimpSubscribe',
    props: {
      action: {}
    },
    data: () => ({
      email: ''
    }),
    methods: {
      subscribe: function (event) {
        const u = '3649778b07e322a50d86d1203'
        const id = '85b3aa5367'
        let data = 'EMAIL= '+this.email+''
        axios({
          method: 'post',
          url: 'https://test.us18.list-manage.com/subscribe/post-json?u='+ u +'&amp;id='+ id +'&c=?',
          data: data,
          dataType: 'json',
          contentType: 'application/json'
        })
        .then(response => {

        })
        .catch(error => {
          console.log(error)
        })
      }
    }
  }
</script>
