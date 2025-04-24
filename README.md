# Rope-Pulling-Game-Simulation
📌 Project Description
This project simulates a Rope Pulling Game using multi-processing and OpenGL for visualization. Two teams compete in a tug-of-war match, each consisting of four players with dynamically changing energy levels. A referee (the parent process) coordinates the rounds, tracks energy levels, and declares the winning team per round based on effort calculations.

This simulation demonstrates real-time inter-process communication, synchronization via signals, pipes, and shared memory in a Linux environment.

🧠 Key Features
Two competing teams, each with 4 players.

Players have energy levels that decrease over time and can randomly "fall" and recover.

Referee process coordinates the game and tracks scores.

Effort values are weighted based on player position in the rope.

OpenGL visualization to display player actions and game progression.

Configuration via external file (user-defined parameters like energy, thresholds, game time).

Game ends when:

A team exceeds a target score.

The game timer runs out.

A team wins 2 consecutive rounds (user-defined).

🛠️ Technologies Used
C language (for logic and multiprocessing)

OpenGL (for graphics)

POSIX (for shared memory, pipes, signals)

GCC, GDB (for compilation and debugging)

Linux OS (Tested on Ubuntu)
⚙️ Installation and Compilation
Make sure you have OpenGL and build tools installed:

bash
sudo apt update
sudo apt install build-essential libgl1-mesa-dev libglu1-mesa-dev freeglut3-dev
To compile:

bash
make
To clean compiled files:

bash
make clean
🚀 Running the Simulation
bash

./rope_game config.txt
Where config.txt contains values like:

txt
initial_energy_range=80-100
energy_decrease_rate_range=1-5
fall_recovery_time_range=2-6
effort_threshold=300
game_duration=120
max_score=5
🧪 Testing and Debugging
Use GDB for debugging:

bash
gcc -g -o rope_game main.c openGL.c -lGL -lGLU -lglut
gdb ./rope_game

📈 Future Improvements
Add sound effects to simulate player falls and win announcements.

Add GUI controls to start/pause/reset the game.

Extend to multiplayer mode over network.

