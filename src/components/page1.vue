<template>
  <form data-toggle="validator" id="myform" role="form" @click="save()"  >
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li><router-link to="/page2">General Infomation</router-link></li>
        <li><router-link to="/page3">Update Profile Picture</router-link></li>
        <li><router-link to="/page4">Payment Method</router-link></li>
        <li><router-link to="/page5">Done!</router-link></li>
      </ul>
        <div class="title">
                <h1>Create Account</h1>
                Glad to see you here!
        </div>
            <div class="user">
                <h3>Account</h3>
                <div class="form-group">
                    <input type="email"  id="InputEmail" class="form-control"   data-error="帳號是無效的，請重新輸入一次。" placeholder="example@email.com" required>
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
                            <input type="password"  id="confirmPassword"  class="form-control" placeholder="Password" data-match-error="這些密碼不符合，請重新輸入一次。"  required data-match="#inputPassword" >
                            <div class="help-block with-errors"></div>
                        </div>
                      </div>
                      <div class="comfirmbtn form-group">
                        <button type="submit" class="btn btn-primary" id="save"  >SUBMIT & NEXT{{111+path}}</button>
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
      path: '/'
    }
  },
  methods: {
    save () {
      $('#myform').validator().on('submit', function (e) {
        if (e.isDefaultPrevented()) {
        } else {
          window.location.href = 'https://s3211t.github.io/F2E-Week6-Validation/#/page2'
          // this.path = '/page2'
        }
      })
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
