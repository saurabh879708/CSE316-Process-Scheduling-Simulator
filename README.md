<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Process Scheduling Simulator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Process Scheduling Simulator</h1>
        
        <div class="input-section">
            <div class="input-group">
                <input type="text" id="processId" placeholder="Process ID">
                <input type="number" id="arrivalTime" placeholder="Arrival Time">
                <input type="number" id="burstTime" placeholder="Burst Time">
                <input type="number" id="priority" placeholder="Priority">
                <button onclick="addProcess()">Add Process</button>
            </div>
            
            <div class="algorithm-select">
                <select id="algorithm">
                    <option value="fcfs">FCFS</option>
                    <option value="sjf">SJF (Non-Preemptive)</option>
                    <option value="srtf">SRTF (Preemptive)</option>
                    <option value="priority">Priority (Non-Preemptive)</option>
                    <option value="rr">Round Robin</option>
                </select>
                <input type="number" id="timeQuantum" placeholder="Time Quantum" style="display: none;">
                <button onclick="startSimulation()">Start Simulation</button>
            </div>
        </div>

        <div class="process-table">
            <table id="processTable">
                <thead>
                    <tr>
                        <th>Process</th>
                        <th>Arrival Time</th>
                        <th>Burst Time</th>
                        <th>Priority</th>
                        <th>Action</th>
                    </tr>
                </thead>
                <tbody></tbody>
            </table>
        </div>

        <div class="results">
            <h2>Gantt Chart</h2>
            <div id="ganttChart" class="gantt-chart"></div>
            <div id="results" class="metrics"></div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
