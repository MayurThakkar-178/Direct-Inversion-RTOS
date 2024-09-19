
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

