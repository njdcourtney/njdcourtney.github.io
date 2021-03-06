---
layout: blog
title: Timeline of the reign of Henry VIII
tags: history

---

<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<script type="text/javascript">
        google.charts.load('current', {'packages':['timeline']});
        google.charts.setOnLoadCallback(drawChart);
        function drawChart() {
          var container = document.getElementById('timeline');
          var chart = new google.visualization.Timeline(container);
          var dataTable = new google.visualization.DataTable();

          dataTable.addColumn({ type: 'string', id: 'Type' });
          dataTable.addColumn({ type: 'string', id: 'Name' });
          dataTable.addColumn({ type: 'date', id: 'Start' });
          dataTable.addColumn({ type: 'date', id: 'End' });
          dataTable.addRows([
                [ 'Life', '2nd Child', new Date(1491, 5, 28), new Date(1502, 3, 1) ],
                [ 'Life', 'Heir', new Date(1502, 3, 2), new Date(1509, 3, 21) ],
                [ 'Life', 'King', new Date(1509, 3, 22), new Date(1547, 0, 28) ],
                [ 'Family', 'Henry VII', new Date(1491, 5, 28), new Date(1509, 3, 21) ],
                [ 'Family', 'Elizabeth of York', new Date(1491, 5, 28), new Date(1503, 1, 11) ],
                [ 'Wife', 'Catherine of Aragon', new Date(1509, 5, 11), new Date(1533, 4, 23) ],
                [ 'Wife', 'Anne Boleyn', new Date(1533, 4, 28), new Date(1536, 4, 17) ],
                [ 'Wife', 'Jane Seymour', new Date(1536, 4, 30), new Date(1537, 9, 24) ],
                [ 'Wife', 'Anne of Cleves', new Date(1540, 0, 6), new Date(1540, 6, 9) ],
                [ 'Wife', 'Catherine Howard', new Date(1540, 6, 28), new Date(1542, 1, 13) ],
                [ 'Wife', 'Catherine Parr', new Date(1543, 6, 12), new Date(1547, 0, 28) ],
                [ 'Executions', 'John Fisher and Sir Thomas More', new Date(1535, 5, 22), new Date(1535, 6, 6) ],
                [ 'Executions', 'Thomas Cromwell', new Date(1540, 6, 28), new Date(1540, 6, 28) ],
        ]);

        var options = {
          timeline: { groupByRowLabel: true }
        };

        chart.draw(dataTable, options);
}
</script>

So we've started rewatching [The Tudors.](https://www.imdb.com/title/tt0758790/) Don't judge, it's been a long lockdown. Anyway, I've been meaning to do this for a while, put together a visual timeline of the life of King Henry VIII

<div id="timeline" style="height: 30em;"></div>

It always surprises me how long he was married to Catherine of Aragon for and how everything goes to pieces towards the end of his reign!