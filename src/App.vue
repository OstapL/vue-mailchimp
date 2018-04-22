<template>
  <div id="app" class="component">
    <Mailchimp action="https://test.us18.list-manage.com/subscribe/post?u=3649778b07e322a50d86d1203&amp;id=85b3aa5367&amp;c=?"></Mailchimp>
  </div>
</template>

<script>
  import Mailchimp from './Mailchimp'

  export default {
    name: 'app',
    data() {
        return {};
    },
    methods: {},
    components: {
      Mailchimp
    }
  }
</script>
