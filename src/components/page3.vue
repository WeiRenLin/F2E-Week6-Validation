<template>
  <form data-toggle="validator" id="myform"  @click="save()" >
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li class="active">General Infomation</li>
        <li class="active">Update Profile Picture</li>
        <li><router-link to="/page4">Payment Method</router-link></li>
        <li><router-link to="/page5">Done!</router-link></li>
      </ul>
        <div class="title">
                <h1>Update Profile Picture</h1>
               We wanna know you more!
        </div>
                  <label class="imageFont">
                       <i class="fa fa-images" style="font-size: 3rem;"></i>
                    <span>UPLOAD UP TO 3 PHOTOS</span>
                    <br>
                    <span>MAXIMUM SIZE: 150*150px</span>
                    <input type="file"    required>
                  </label>
                    <div class="help-block with-errors"></div>
                    <div class="warning">
                      <i class="fas fa-exclamation-triangle"></i>
                      <span>ONE FILE IS OVER THE MAXIMUM SIZE</span>
                    </div>
                    <div id="image">
                      <img src="../../image/image1.jpg">
                      <img src="../../image/image2.jpg">
                      <img src="../../image/image3.jpeg">
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
  name: 'page3',
  data () {
    return {
    }
  },
  methods: {
    save () {
      $('#myform').validator().on('submit', function (e) {
        if (e.isDefaultPrevented()) {
        } else {
          window.location.href = 'https://s3211t.github.io/F2E-Week6-Validation/#/page4'
        }
      })
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
