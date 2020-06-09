<script>
</script>

<style>
/* start: style for nav bar */
.nav{
  border:1px solid #ccc;
  border-width:1px 0;
  list-style:none;
  margin:0;
  padding:0;
  text-align:center;
	background-color: #007acc;
	/* position: fixed; */
	bottom: 0;
	width: auto;
}
.nav li{
  display:inline;
	/* float: left; */
	/* border: 1px solid #7995a1; */
	color: black;
	background: #007acc;	
}
.nav a{
  display:inline-block;
  padding:10px;
	color: white;
	text-align: center;
	padding: 14px 16px;
	text-decoration: none;
}


.nav li a:hover:not(.active) {
  background-color: #111;
}

.active {
  background-color: #004777;
}
/* end: style for nav bar */ 
</style>

<ul class="nav">
		<li><a href="dashboard.html">Dashboard</a></li>
		<li><a href="townreport.html">Town Report</a></li>
		<li><a href="admin.html">Admin</a></li>
		<li><a href="followup.html">Follow Up</a></li>
		<li><a href="PageUserProf.svelte">User Profile</a></li>
		<li><a class="active" href="index.html">Sign Out</a></li>
	</ul>