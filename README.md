# Electrical Load Monitoring System

A simple console-based C++ program for tracking household appliances, calculating daily energy usage, and estimating electricity costs.

---

## Overview

This application allows users to:

- Add electrical appliances with their power rating and usage hours
- View all registered appliances
- Search for a specific appliance
- Calculate total daily energy consumption
- Estimate daily and monthly electricity costs
- Save appliance data and billing summaries to files

The program automatically loads saved appliance data when it starts.

---

## Technologies

- C++
- Standard Library:
  - iostream
  - fstream
  - vector
  - iomanip
  - ctime
  - limits

---

## Project Structure

```
Project Folder
 ├── main.cpp
 ├── appliances.txt          (created automatically)
 ├── billing_summary.txt     (created when saving reports)
 └── README.md
```

---

## Compilation and Execution

### Using g++

```
g++ main.cpp -o load_monitor
./load_monitor
```

### Using Visual Studio

1. Create a new Console Application project.
2. Replace the default source file with `main.cpp`.
3. Build and run the project.

---

## How It Works

### Registering an Appliance

You will be asked to enter:

- Appliance name
- Power rating in watts
- Hours used per day

Daily energy consumption is calculated as:

```
kWh per day = (Watts / 1000) × Hours
```

---

### Calculating the Bill

When calculating the bill, you will enter:

- Tariff per kWh

The program computes:

- Total daily energy consumption
- Daily electricity cost
- Estimated monthly cost (30 days)

You can choose to save the billing summary to a file.

---

## Data Storage

- `appliances.txt` stores all registered appliances.
- `billing_summary.txt` stores saved billing reports with timestamps.

---

## Example Output

```
TV - 0.80 kWh/day
Fan - 0.75 kWh/day

Total Daily Energy: 1.55 kWh
Daily Cost: 0.31
Estimated Monthly Cost (30 days): 9.30
```

---

## Possible Improvements

- Edit or delete appliances
- Case-insensitive search
- Annual cost estimation
- Export reports to CSV
- Add a graphical interface

---

## License

This project is free to use for educational purposes.