# Table showing action usage

{% assign actionlist = site.data.syntax | map: "name" %}

<canvas id="myChart" style="width:100%;max-width:600px"></canvas>

<script>
var xValues = [ {{ actionlist | join: ", " }} ];
var yValues = [3, 7, 8, 4, 5, 2, 0];
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



