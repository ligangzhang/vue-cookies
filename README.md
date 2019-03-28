# vue-cookies
A simple vue.js plugin for handling browser cookies

## install
cnpm install vue-cookies --save

## entry file
import Vue from 'vue';

import VueCookies from 'vue-cookies';

Vue.use(VueCookies);

## usage

### set global config
this.$cookies.config('7d', '/');  //expireTime: 7 days, path=/

### get cookie
this.$cookies.get('keyName');

### set cookie
this.$cookies.set(keyName, value[, expireTimes[, path[, domain[, secure]]]])

this.$cookies.set('age', '8');

### support json
var user = { id:1, name:'Journal',session:'25j_7Sl6xDq2Kc3ym0fmrSSk2xV2XkUkX' };
this.$cookies.set('user',user);
// print user name
console.log(this.$cookies.get('user').name)

### remove a cookie
$cookies.remove(keyName [, path [, domain]])  // return this

### exist a cookie name
$cookies.isKey(keyName)  // return false or true

### get all cookies name
this.$cookies.keys()  // return a array

