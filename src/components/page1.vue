<template>
  <form data-toggle="validator" id="myform" role="form" @click="save()"  >
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li>General Infomation</li>
        <li>Update Profile Picture</li>
        <li>Payment Method</li>
        <li>Done!</li>
      </ul>
        <div class="title">
                <h1>Create Account</h1>
                Glad to see you here!
        </div>
            <div class="user">
                <h3>Account</h3>
                <div class="form-group">
                    <input type="email"  id="InputEmail" class="form-control"   data-error="that email address is invalid" placeholder="example@email.com" required>
                    <div class="help-block with-errors"></div>
                </div>
              </div>
              <div class="password">
                    <h3>Password</h3>
                    <div class="form-group">
                        <input type="password"  id="inputPassword" class="form-control" data-minlength="6"  placeholder="Password"  required>
                        <div class="help-block with-errors"></div>
                    </div>
                  </div>
                  <div class="comfirmpd">
                        <h3>Comfirm Password</h3>
                        <div class="form-group">
                            <input type="password"  id="confirmPassword"  class="form-control" placeholder="Password" data-match-error="Whoops, these don't match"  required data-match="#inputPassword" >
                            <div class="help-block with-errors"></div>
                        </div>
                      </div>
                      <div class="comfirmbtn form-group">
                        <button type="submit" class="btn btn-primary" id="save"  >SUBMIT & NEXT</button>
                      </div>
        </form>
</template>
<script>
import $ from 'jquery'
require('bootstrap-validator')
export default {
  name: 'page1',
  data () {
    return {
    }
  },
  methods: {
    save () {
      $('#myform').validator().on('submit', function (e) {
        window.location = '/page2'
      })
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
