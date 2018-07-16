<template>
    <form data-toggle="validator" id="myform" @click="save()">
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li class="active">General Infomation</li>
        <li class="active">Update Profile Picture</li>
        <li class="active">Payment Method</li>
        <li>Done!</li>
      </ul>
        <div class="title">
                <h1>General Infomation</h1>
                Glad to see you here!
        </div>
        <div class="page2">
                <div class="group form-group">
                <h3>Card Number</h3>
                    <input type="text"   placeholder="1234 5678 9012 3456" style="width:100%" pattern="[0-9]{13,16}" required>
                    <div class="help-block with-errors"></div>
              </div>
                <div class="group half" form-group>
                <h3>Cardholder Name</h3>
                    <input type="text"   placeholder="EXAMPLE NAME">
                    <div class="help-block with-errors"></div>
                </div>
              <div class="group half form-group">
                    <h3>Bank Name</h3>
                            <input type="text"   placeholder="EXAMPLE BANK">
                            <div class="help-block with-errors"></div>
                  </div>
                  <div class="group third form-group">
                    <h3>CVV</h3>
                            <input type="text"  id="cvv" placeholder="123" >
                            <div class="help-block with-errors"></div>
                  </div>
                  <div class="group third form-group">
                      <h3 style="margin-left:-13px">Expire Date</h3>
                            <input type="text"  id="twothird" placeholder="Dist">
                            <div class="help-block with-errors"></div>
                  </div>
                  <div class="group third form-group">
                            <input type="text"  id="thirdthird" placeholder="Address Detail">
                            <div class="help-block with-errors"></div>
                  </div>
        </div>
         <div class="comfirmbtn form-group">
                        <button type="submit" class="btn btn-primary" id="save"  >Done</button>
                      </div>
        </form>
</template>
<script>
import $ from 'jquery'
require('bootstrap-validator')
export default {
  name: 'page4',
  data () {
    return {
    }
  },
  methods: {
    save () {
      $('#myform').validator().on('submit', function (e) {
        if (e.isDefaultPrevented()) {
        } else {
          window.location = '/?#/page5'
        }
      })
    }
  }
}
</script>
