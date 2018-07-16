<template>
    <form data-toggle="validator" id="myform" @click="save()">
    <ul id="progressbar">
        <li class="active">Create Account</li>
        <li class="active">General Infomation</li>
        <li>Update Profile Picture</li>
        <li>Payment Method</li>
        <li>Done!</li>
      </ul>
        <div class="title">
                <h1>General Infomation</h1>
                Glad to see you here!
        </div>
        <div class="page2">
                <div class="group half">
                <h3>Name (optional)</h3>
                    <input type="text"   placeholder="Example Name">
              </div>
              <div class="group half form-group">
                <h3>Phone*</h3>
                    <input type="text"   placeholder="0912 345 678" required>
                    <div class="help-block with-errors"></div>
              </div>
              <div class="group">
                    <h3>Birth Date (optional)</h3>
                            <input type="date"  id="Year" placeholder="YYYY"  />
                  </div>
                  <div class="group address form-group">
                    <h3>Address*</h3>
                            <input type="text"  id="City" placeholder="City"  required/>
                            <div class="help-block with-errors"></div>
                  </div>
                  <div class="group address form-group">
                            <input type="text"  id="Dist" placeholder="Dist" required />
                            <div class="help-block with-errors"></div>
                  </div>
                  <div class="group form-group">
                            <input type="text"  id="AddressDe" placeholder="Address Detail" required />
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
  name: 'page2',
  data () {
    return {
    }
  },
  methods: {
    save () {
      $('#myform').validator().on('submit', function (e) {
        if (e.isDefaultPrevented()) {
        } else {
          window.location = '/?#/page3'
        }
      })
    }
  }
}
</script>
