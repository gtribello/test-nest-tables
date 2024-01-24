# Table showing action usage

{% assign actionlist = site.data.syntax | map: "name" %}

{% for item in site.data.tabledata %}
   {% assign actions = item.actions | split: ", " %}
   {% for a in actions %}
      {% assign act=a | strip %} 
      {% for s in site.data.syntax %}
         {{ s.name }} 
         {{ act }}
         {% if act contains s.name %} 
             {% assign s.number=s.number | plus: 1 }
             {{ act }}
             {{ s.name }}
             {{ s.number }}  
             {% break %}
         {% else %}
             {% continue %} 
         {% endif %}
      {% endfor %} 
   {% endfor %}
{% endfor %}

{% assign actionnumber = site.data.syntax | map: "number" %}


<canvas id="myChart" style="width:100%;max-width:600px"></canvas>

<script>
var xValues = [ {{ actionlist | join: '", "' | prepend: '"' | append: '"' }} ];
var yValues = [ {{ actionnumber | join: "," }} ];
var barColors = "red";

new Chart("myChart", {
  type: "horizontalBar",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: barColors,
      data: yValues
    }]
  },
  options: {
    maintainAspectRatio: false,
    legend: {display: false},
    title: {
      display: true,
      text: "Number of lessons using this action"
    }
  }
});
</script>



