# Table showing action usage

{% assign actionlist = site.data.actionlist0 | map: "name" %}
{% assign actionno = site.data.actionlist0 | map: "number" %}
{% assign actionno1 = site.data.actionlist1 | map: "number" %}
{% assign nactions=actionno0.size %}

{% for i in (0..nactions) %}
   {{ actionno[i] }}
   {% assign actionno[i]=actionno[i] | plus: actionno1[i] %}  
   {{ actionno[i] ))
{% endfor %}


<canvas id="myChart" style="width:100%;max-width:600px"></canvas>

<script>
var xValues = [ {{ actionlist | join: '", "' | prepend: '"' | append: '"' }} ];
var yValues = [ {{ actionno | join: ", " }} ];
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



