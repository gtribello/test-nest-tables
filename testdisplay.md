# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

<script>
async function getSyntax() {
  const response = await fetch('./syntax.0.json')
  return response.json();
}
  
$(document).ready(function() {
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="action" ) {
      const syntax = getSyntax();
      console.log({ syntax });
      document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use </br></br>" + searchfor[1] + " (action) " + "</b>";
  }  
});
</script>
