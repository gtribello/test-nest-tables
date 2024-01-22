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
  "columnDefs": [ 
     { "targets": 4, "visible": false }
  ],
  language: { search: '', searchPlaceholder: "Search project..." },
  buttons: [
        'copy', 'excel', 'pdf'
  ],
  "order": [[ 0, "desc" ]]
  });
$('#browse-table-searchbar').keyup(function () {
  table.search( this.value ).draw();
  });
});
</script>
