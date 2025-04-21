# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

<script>
$(document).ready(function() {
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="action" ) {
      fetch('./syntax.0.json')
        .then((response) => response.json())
        .then((json) => console.log(json));
      document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use \n\n" + searchfor[1] + " (action) " + plumedsyntax[ searchfor[1] ]["description"] + "</b>";
  }  
});
</script>
