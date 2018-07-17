<template>
    <form data-toggle="validator" id="myform" @click="save()">
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li class="active">General Infomation</li>
        <li class="active">Update Profile Picture</li>
        <li class="active">Payment Method</li>
        <li class="active">Done!</li>
      </ul>
        <div class="title">
                <h1>Congratulations</h1>
                Now you’re one of us!
        </div>
        <div class="page5">
                <i class="fa fa-smile" style="font-size:10rem;color:#BEE1FF"></i>
                <br>
                <span style="margin-top:25px;">Redirected to homepage after 5 seconds…</span>
        </div>
        </form>
</template>
<script>
require('bootstrap-validator')
export default {
  name: 'page4',
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>
