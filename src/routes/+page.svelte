<h1>Fed Org Charts</h1>
<div id="chart_div"></div>

<svelte:head>
    <script src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
        google.charts.load('current', {packages:["orgchart"]});
        google.charts.setOnLoadCallback(drawChart);
  
        function drawChart() {
          var data = new google.visualization.DataTable();
          data.addColumn('string', 'Name');
          data.addColumn('string', 'Parent');
          data.addColumn('string', 'ToolTip');
  
          // For each orgchart box, provide the name, manager, and tooltip to show.
          data.addRows([
            ['The Constitution', '', 'The Federal Constitution'],
            ['Legislative Branch', 'The Constitution', ''],
            ['Executive Branch', 'The Constitution', ''],
            ['Judicial Branch', 'The Constitution', ''],

            ['Department of Agriculture', 'Executive Branch', ''],
            ['Department of Commerce', 'Executive Branch', ''],
            ['Department of Defense', 'Executive Branch', ''],
            ['Department of Education', 'Executive Branch', ''],
            ['Department of Energy', 'Executive Branch', ''],
            ['Department of Health and Human Services', 'Executive Branch', ''],
            ['Department of Homeland Security', 'Executive Branch', ''],
            ['Department of Housing and Urban Development', 'Executive Branch', ''],
            ['Department of the Interior', 'Executive Branch', ''],
            ['Department of Justice', 'Executive Branch', ''],
            ['Department of Labor', 'Executive Branch', ''],
            ['Department of State', 'Executive Branch', ''],
            ['Department of Transportation', 'Executive Branch', ''],
            ['Department of the Treasury', 'Executive Branch', ''],
            ['Department of Veterans Affairs', 'Executive Branch', '']
          ]);
  
          // Create the chart.
          var chart = new google.visualization.OrgChart(document.getElementById('chart_div'));
          // Draw the chart, setting the allowHtml option to true for the tooltips.
          chart.draw(data, {'allowHtml':true});
        }
     </script>
</svelte:head>