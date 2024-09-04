# SmartChess
The aim of the thesis is to construct a chess robot capable of playing fully autonomously with
humans. It stemmed from a passion for both chess and robotics. Particularly, the knowledge
gained from elective courses in robotics and technical subjects proved invaluable, especially
in 3D design and programming.
To detect human moves, photoresistors were installed on each of the 64 chess squares. These
sensors measure the presence or absence of a chess piece on each square, providing an
analog value that is then compared with a matrix of previous readings. This results in a
readable chess move, such as "e2e4," which is then transmitted serially to the Raspberry Pi,
serving as the central control unit. For instance, "e2e4" indicates moving the chess piece from
square "e2" to "e4," advancing it two squares forward. The decision to use photoresistors came
after evaluating an initial prototype that utilized reed switches, but encountered issues with the
magnets being too strong.
To generate chess moves, the Stockfish chess engine was utilized on the Raspberry Pi, as it
proved to be highly suitable for the project's objectives due to its precision and minimal
resource requirements. After processing human moves, a countermove is generated and
transmitted serially to the Arduino.
The chess pieces are moved from the underside of the self-constructed chessboard using
electromagnets. The material of the chessboard is acrylic glass, allowing insight into the
electronics and motors, thereby enhancing understanding of the chess robot's functionality.
For motor control, the open-source firmware GRBL was employed, primarily due to its
widespread use in hobby projects and its simple control interface for stepper motors via
custom-written software. A part of a Prusa 3D printer served as the framework for the chess
robot, saving time in planning for a custom framework and allowing for easy modification and
3D printing of components such as chessboard holders and motor mounts.
Additionally, the chess game can be viewed live on a webpage hosted on the Raspberry Pi,
where various settings such as player color (black/white) and difficulty level can be adjusted,
and the game can be paused, restarted, or reset.

![grafik](https://github.com/user-attachments/assets/cee9e0f0-7c90-4800-a771-61ee6e99812b)
