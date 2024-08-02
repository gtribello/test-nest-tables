# Test table

{:#browse-table .display}
| ID | Name | Instructors | Description | Actions |
|:--------:|:--------:|:---------:|:---------:|:---------:|:---------:|:---------:|
{% for item in site.data.tabledata %}| {{ item.id }} | [{{ item.title }}]({{ item.path }}) | {{ item.instructors | split: " " | last}} {{ item.instructors | split: " " | first | slice: 0}}. | {{ item.description }} | {{ item.actions }}
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
  table.search( this.value ).draw();
  });
  hu = window.location.search.substring(1);
  searchfor = hu.split("=");
  if( searchfor[0]=="search" ) {
      allterms = searchfor[1].split(' ');
      alert( allterms );
      finalterm = allterms[0];
      for(let i=1; i<allterms.length(); i++) { finalterm = finalterm + '&nbsp' + allterms[i]; }
      table.search( finalterm ).draw();
  }
});
</script>
