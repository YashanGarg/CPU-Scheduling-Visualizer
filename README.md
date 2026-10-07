# CPU Scheduling Visualizer

An interactive, in-browser tool for exploring how CPU scheduling algorithms work. Enter a set of processes, pick an algorithm, and get a Gantt chart, a per-process timeline, a step-by-step queue log, and a table of completion, turnaround, waiting and response times.

No build step and no dependencies to install: open `index.html` in a browser.

## Features

- Algorithms: FCFS, SJF, SRTF, Round Robin, Priority (preemptive), Priority (non-preemptive)
- Processes with multiple CPU / I/O burst phases (use the `+` / `-` buttons on a row)
- Configurable arrival times, priorities (1 = high or low, switchable), time quantum and context-switch time
- Gantt chart and timeline chart (Google Charts), averages and per-process metrics
- Ties are broken by process ID

## Run it

```bash
git clone <your-repo-url>
cd CPU-Scheduling-Visualizer
# either open index.html directly, or serve it locally:
python3 -m http.server 8000   # then visit http://localhost:8000
```

An internet connection is needed because Bootstrap, Font Awesome and Google Charts are loaded from CDNs.

## Project structure

```
.
├── index.html       # page markup and input form
├── css/
│   └── style.css    # styles
└── js/
    └── main.js      # UI logic, scheduling algorithms, chart rendering
```

## Notes on the scheduler

- When burst time is the criterion, total CPU burst time of the process is used.
- Context switch time is not applied at the very start or end of the schedule.

## Tech

HTML, CSS, vanilla JavaScript, Bootstrap 5, Google Charts.

## Author

Yashan Garg

Originally built as a class project on CPU Scheduling Algorithms.
