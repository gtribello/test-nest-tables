# Table showing action usage

<canvas id="myChart" style="width:100%;max-width:600px"></canvas>

<script>
var xValues = ["DISTANCE", "ANGLES", "METAD", "COM", "BIASVALUE"];
var yValues = [3, 7, 8, 4, 5];
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
    legend: {display: false},
    title: {
      display: true,
      text: "Number of lessons using this action"
    }
  }
});
</script>



