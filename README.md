# GNSS Positioning Engine

## Project Overview

This project is a GNSS positioning engine designed to process raw data from a 
u-blox F9P receiver in .ubx format and compute a Position, Velocity, and Time 
(PVT) solution. Initially, the implementation will be limited to GPS L1 C/A 
signals and will use a simple least-squares solver (excluding Kalman filtering).

## Features

* Read and parse .ubx files from u-blox F9P GNSS receivers.
* Extract raw GNSS measurements including pseudorange and carrier phase data.
* Compute a basic PVT solution using a least-squares method.
* Support for GPS L1 C/A signals (future updates may include other 
constellations and frequencies).
* Standalone Python implementation without reliance on external positioning 
services.

## Installation

# Prerequisites

Ensure you have Python installed (recommended version: 3.12+). Install 
required dependencies using:

`pip install -r requirements.txt`

## Usage

1. **Prepare Input Data**: Collect .ubx files from a u-blox F9P receiver.
2. **Run the GNSS Engine**: Execute the script to process the raw GNSS data and 
compute PVT solutions.

`python gnss_solver.py --input data/sample.ubx`

3. **Analyze Results**: The computed PVT solution will be output in a structured 
format (e.g., CSV, JSON, or console log).

## Project Structure

📂 gnss-positioning-engine
├── 📂 data               # Sample .ubx files
├── 📂 src                # Source code
│   ├── ubx_parser.py    # UBX file parser
│   ├── gnss_solver.py   # Least-squares solver
├── requirements.txt      # Required Python libraries
├── README.md            # Project documentation

## Contribution

Contributions are welcome! Feel free to submit issues and pull requests.

## License

This project is licensed under the GNU 3.0 License.

