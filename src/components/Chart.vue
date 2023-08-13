<script setup>
    import Chart from 'chart.js/auto';
    import { onMounted } from 'vue';
    
    const ctx = document.getElementById('myChart');

    new Chart(ctx, {
        type: 'pie',
        data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            borderWidth: 1
        }]
        },
        options: {
        scales: {
            y: {
            beginAtZero: true
            }
        }
        }
    });
</script>

<template>
    <div class="container my-5">
        <div class="card">
            <div class="card-body">
                <div>
                    <h1>Bar Chart</h1>
                    <canvas id="myChart"></canvas>
                </div>
            </div>
        </div>
    </div>
</template>