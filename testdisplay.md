# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

<script>
$(document).ready(function() {
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="action" ) {
      fetch("./syntax.0.json")
        .then(response => {
        if (!response.ok) {
          throw new Error('Network response was not ok');
        }
        return response.json();
        })
        .then(data => document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use </br></br>" + searchfor[1] + " (action): " + data[ searchfor[1] ]["description"] + ". <a href=\"" + data[ searchfor[1] ]["hyperlink"] + "\">More details</a></b>" )
      
  }  
});
</script>
