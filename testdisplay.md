# Test table

{% raw %}
<div id="diplay_description"> </div>
{% endraw %}

{:#browse-table .display}
| ID | Name | Instructors | Description | Actions |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|:---------:|
{% for item in site.data.tabledata %}
{% if item.id == "23.004" %}
| {{ item.id }} | [{{ item.title }}]({{ item.path }}) | {{ item.instructors | split: " " | last}} {{ item.instructors | split: " " | first | slice: 0}}. | {{ item.description }} | {{ item.actions }}
{% else %}
{% continue %}
{% endif %}
{% endfor %}

<script>
$(document).ready(function() {
var table = $('#browse-table').DataTable({
  "dom": '<"search"f><"top"il>rt<"bottom"Bp><"clear">',
  language: { search: '', searchPlaceholder: "Search project..." },
  buttons: [
        'copy', 'excel', 'pdf'
  ],
  "columnDefs": [ 
     { "targets": 4, "visible": false }
  ],
  "order": [[ 0, "desc" ]]
  });
$('#browse-table-searchbar').keyup(function () {
  var page = location.href;
  location.replace( page.split("?")[0] );
  table.search( this.value ).draw();
  });
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="search" ) {
      table.search( searchfor[1].replace("%20"," ") ).draw();
  } else if( searchfor[0]=="action" ) {
      alert( "Hello gareth " + searchfor[1] );
      document.getElementById("diplay_description").innerHTML = "<b>Showing lessons that use \n\n" + searchfor[1] + " (action) " + plumedsyntax[searchfor[1]]["description"] + "</b>";
});
</script>
