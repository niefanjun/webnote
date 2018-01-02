<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: 'app'
}
</script>
<script>
	(function(j) {
	  var h = j.sdkUrl,
	    a = j.name,
	    d = this,
	    g = d.document,
	    f = null,
	    e = null;
	  d.AGENT20170621 = a;
	  d[a] = d[a] || function(i) {
	    return function() {
	      (d[a]._agenti = d[a]._agenti || []).push([i, arguments])
	    }
	  };
	  var b = ["track", "trackSignup", "userIdentify"];
	  for (var c = 0; c < b.length; c++) {
	    d[a][b[c]] = d[a].call(null, b[c])
	  }
	  if (!d[a].lt) {
	    f = g.createElement("script"), e = g.getElementsByTagName("script")[0];
	    f.async = true;
	    f.src = h;
	    e.parentNode.insertBefore(f, e);
	    d[a].lt = 1 * new Date();
	    d[a].para = j
	  }
	})({
	  sdkUrl: location.protocol + "//v2.web.ue.zhubajie.la/api/v1/agent/info/F25GH546FH8DG5R25W2W8G2RH8N1W4G6/8GG6S29FW8WFGSWHH1GR4DD5FD2NG5NR",
	  sendLimit: 1,
	  showLog: true,
	  name: "nfjtest",
	  autoTrack: true,
	  apiHost: location.protocol + "//v2.web.ue.zhubajie.la",
	  appToken: "8GG6S29FW8WFGSWHH1GR4DD5FD2NG5NR"
	});
</script>
<style lang="scss">
@import "./style/style";
</style>