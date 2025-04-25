# System Monitoring Script with Report Generation

This project provides a bash script (`monitor.sh`) that monitors various system metrics like CPU usage, memory usage, disk usage, GPU status, and temperature. It also generates HTML and Markdown reports, providing real-time alerts and logging. The script integrates with `Zenity` for graphical user interface (GUI) alerts.

## Features

- **Real-time Alerts**: Alerts for critical CPU, memory, disk usage, and temperature.
- **Report Generation**: Generates HTML and Markdown reports with detailed metrics.
- **GPU Monitoring**: Supports NVIDIA and AMD GPU monitoring.
- **Smart Status**: Checks the SMART status of disks.
- **Interactive Dashboard**: Allows the user to view historical reports and run system monitoring via a simple GUI dashboard.

## Project Structure

```
/app/
├── monitor.sh                        // Main monitoring script
├── generate_md_report.py             // Python script to generate markdown reports
└── Dockerfile                        // Dockerfile for containerization
```


## Requirements

- **Bash**
- **Zenity**: For GUI-based alerts
- **lm-sensors**: For temperature monitoring
- **nvidia-smi/rocm-smi**: For GPU monitoring
- **smartmontools**: For SMART status
- **Python 3**: For report generation

## Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Install dependencies on a Debian-based system:
   ```bash
   sudo apt-get install wget gnupg2 lm-sensors smartmontools zenity python3
   ```
3. Run the script:
   ```bash
   ./monitor.sh
   ```
4. For Docker users, you can build and run the Docker container:
   ```bash
   docker build -t system-monitoring .
   docker run -d --name monitor system-monitoring
   ```

## Usage

- Once the container is running, you can interact with the monitoring dashboard and generate system reports as required.

  
---

Feel free to fork, contribute, or use this for educational purposes!
