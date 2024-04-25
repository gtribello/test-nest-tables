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
  searchfor = gy[i].split("=");
  if( searchfor==null ) {
  } else {
      alert( searchfor );
  }
});

window.onload = function() {
function querySt(ji) {
 hu = window.location.search.substring(1); 
 gy = hu.split("&");
 for (i=0;i<gy.length;i++) { 
    ft = gy[i].split("="); 
    if (ft[0] == ji) { 
        return ft[1]; 
    } 
 } 
} 
var fieldName = querySt("fieldName");
if( fieldName==null){ 
 } else { 
    document.getElementById('browse-table').search( fieldName ).draw(); 
 } 
}
</script>
