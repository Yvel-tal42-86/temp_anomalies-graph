
    


    <script src="https://cdn.jsdelivr.net/npm/chart.js@3.2.1/dist/chart.min.js"></script>

    <canvas id="chart" width="800" height="450">
        <script>
            const ctx = document.getElementById('chart').getContext('2d');
            const myChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: [] ,
                    datasets: [{
                        label: 'Temperature anomalies',
                        backgroundColor: 'rgba(255, 99, 132, 0.2)',
                        data: [] ,
                        borderColor: 'rgba(255, 99, 132, 1)',
                        borderWidth: 1
                    }]
                },
                type: 'line',
                fill: false,
                data: data,
                options: {
                    scales: {
                        y: {
                            ticks: {
                                // Include a dollar sign in the ticks
                                callback: function (value, index, values) {
                                    return value + "°"
                                }
                            }
                        }
                    }
                }
            });
        </script>
    </canvas>

