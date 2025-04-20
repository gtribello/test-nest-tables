# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

<script>
$(document).ready(function() {
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="search" ) {
      table.search( searchfor[1].replace("%20"," ") ).draw();
  } else if( searchfor[0]=="action" ) {
      alert( "Hello gareth" );
      document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use \n\n" + searchfor[1] + " (action) " + plumedsyntax[searchfor[1]]["description"] + "</b>";
  }  
});
</script>
