<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Direct Inversion PCP Scheduling</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #e9ecef;
            color: #333;
        }
        h1 {
            color: #4a90e2;
            text-align: center;
        }
        h3 {
            color: #343a40;
        }
        form {
            background-color: #fff;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
            margin-bottom: 20px;
        }
        input {
            margin: 5px 0;
            padding: 8px;
            width: calc(100% - 18px);
            border: 1px solid #ced4da;
            border-radius: 4px;
        }
        button {
            padding: 10px 15px;
            color: #fff;
            background-color: #007bff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        table, th, td {
            border: 1px solid #ccc;
        }
        th, td {
            padding: 10px;
            text-align: center;
            background-color: #f8f9fa;
        }
        th {
            background-color: #007bff;
            color: white;
        }
        #ganttChart {
            width: 100%;
            height: 60px;
            border: 1px solid #ccc;
            background-color: #fff;
            position: relative;
            overflow: hidden;
            margin-bottom: 20px;
        }
        .task {
            position: absolute;
            height: 100%;
            color: white;
            text-align: center;
            line-height: 60px;
            border-radius: 4px;
        }
        .task1 { background-color: #4caf50; }
        .task2 { background-color: #2196F3; }
        .task3 { background-color: #ff9800; }
        .task4 { background-color: #f44336; }
        .task5 { background-color: #9c27b0; }
    </style>
</head>
<body>

<h1>Direct Inversion PCP Scheduling</h1>

<form id="taskForm">
    <h3>Add Task</h3>
    <label for="taskName">Task Name:</label>
    <input type="text" id="taskName" required>
    <label for="priority">Priority:</label>
    <input type="number" id="priority" required>
    <label for="period">Period (ms):</label>
    <input type="number" id="period" required>
    <label for="executionTime">Execution Time (ms):</label>
    <input type="number" id="executionTime" required>
    <button type="submit">Add Task</button>
</form>

<h3>Tasks</h3>
<table id="taskTable">
    <thead>
        <tr>
            <th>Task Name</th>
            <th>Priority</th>
            <th>Period</th>
            <th>Execution Time</th>
        </tr>
    </thead>
    <tbody>
    </tbody>
</table>

<h3>Gantt Chart</h3>
<div id="ganttChart"></div>

<h3>Schedule</h3>
<pre id="scheduleOutput"></pre>

<script>
    const tasks = [];
    const scheduleOutput = document.getElementById('scheduleOutput');
    const ganttChart = document.getElementById('ganttChart');

    document.getElementById('taskForm').addEventListener('submit', function(event) {
        event.preventDefault();
        
        const taskName = document.getElementById('taskName').value;
        const priority = parseInt(document.getElementById('priority').value);
        const period = parseInt(document.getElementById('period').value);
        const executionTime = parseInt(document.getElementById('executionTime').value);
        
        const task = {
            name: taskName,
            priority: priority,
            period: period,
            executionTime: executionTime,
            className: `task${tasks.length % 5 + 1}` // Cycle through 5 colors
        };
        
        tasks.push(task);
        updateTaskTable();
        scheduleTasks();
        
        // Reset form
        this.reset();
    });

    function updateTaskTable() {
        const tableBody = document.getElementById('taskTable').querySelector('tbody');
        tableBody.innerHTML = '';
        
        tasks.forEach(task => {
            const row = document.createElement('tr');
            row.innerHTML = `
                <td>${task.name}</td>
                <td>${task.priority}</td>
                <td>${task.period}</td>
                <td>${task.executionTime}</td>
            `;
            tableBody.appendChild(row);
        });
    }

    function scheduleTasks() {
        const schedule = [];
        let time = 0;

        // Clear Gantt Chart
        ganttChart.innerHTML = '';

        while (time < 100) { // Schedule for 100 ms
            const runnableTasks = tasks.filter(task => time % task.period === 0);
            runnableTasks.sort((a, b) => a.priority - b.priority); // Higher priority comes first

            for (const task of runnableTasks) {
                for (let i = 0; i < task.executionTime; i++) {
                    if (time + i < 100) {
                        schedule.push(`${task.name} at ${time + i} ms`);
                    }
                }

                // Create Gantt Chart Block
                const taskBlock = document.createElement('div');
                taskBlock.className = `task ${task.className}`;
                taskBlock.style.width = (task.executionTime * 10) + 'px'; // Scale for visibility
                taskBlock.style.left = (time * 10) + 'px'; // Scale for visibility
                taskBlock.innerText = task.name;
                ganttChart.appendChild(taskBlock);

                time += task.executionTime; // Move time forward by execution time
                break; // Re-schedule from the beginning
            }
            time++;
        }

        scheduleOutput.textContent = schedule.join('\n');
    }
</script>

</body>
</html>
