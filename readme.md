# Ant Farm Simulation

This is a Go program to simulate the movement of ants in a farm. The program reads the farm configuration from a file, processes the data, and simulates the movement of ants from a start room to an end room through various paths.

## Features

- Reads farm configuration from a file
- Supports multiple rooms and tunnels
- Simulates ant movements through the shortest paths
- Ensures no overlap in paths
- Outputs all paths, filtered paths, and ant movements

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/ant-farm-simulation.git
    cd ant-farm-simulation
    ```

2. **Build the project:**
    ```bash
    go build main.go
    ```

## Usage

1. **Prepare your input file** in the following format:
    - First line: Number of ants
    - Room definitions: `room_name x_coord y_coord`
    - Start room: `##start` followed by `room_name x_coord y_coord`
    - End room: `##end` followed by `room_name x_coord y_coord`
    - Tunnel definitions: `room1-room2`

    Example:
    ```
    3
    ##start
    A 1 1
    ##end
    B 2 2
    C 3 3
    A-B
    B-C
    ```

2. **Run the simulation:**
    ```bash
    ./main inputfile.txt
    ```

3. **Output:**
    - All paths from start to end
    - Filtered paths without overlapping
    - Ant movements step-by-step

## Example

Given the following input file `farm.txt`:

3
##start
A 1 1
##end
B 2 2
C 3 3
A-B
B-C

Running the simulation:

```bash
./main example00.txt,example01.txt...example07.txt,badexample00.txt,badexapmle01.txt

Produces output similar to:

All paths from start room to end room:
Path 1: [A B]
Path 2: [A B C]

Filtered Paths:
Path 1: [A B]
Path 2: [A B C]

Ant Movements:
L1-B L2-B
L1-C

License
This project is licensed under the MIT License.