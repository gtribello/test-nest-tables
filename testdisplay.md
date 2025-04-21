# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

<script>
$(document).ready(function() {
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="action" ) {
      try 
      {
      response = await fetch('./syntax.0.json');
      syntax = await response.json();
      console.log(syntax);
      document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use </br></br>" + searchfor[1] + " (action) " + "</b>";
      }
      catch(error)
      {
      }
  }  
});
</script>
