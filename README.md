# PokerGame

A C++ Poker game project developed as part of the "Cơ sở lập trình" (Fundamentals of Programming) course at the University of Science, VNU-HCM. The project demonstrates core OOP concepts, game logic implementation, and graphical interface programming with SDL2.

## Overview

This application simulates a Poker game supporting multiple modes:
- **Basic Poker**: Each player is dealt 5 cards, and the winner is determined based on standard Poker hand rankings.
- **Five-Card Stud**: Players receive 2 cards, and 5 community cards are dealt.

The game allows 2–5 players to play against the computer and maintains player statistics (wins, games played).

## Features
Object-Oriented Design with modular classes:
- `Player`, `Card`, `Deck`, `Table`, `Game`, etc.
- Clear separation of UI, game logic, and data handling.

Graphical User Interface:
- Built with SDL2, supporting textures, fonts, and audio.
- Dynamic screens for menu, gameplay, and results.

Game Mechanics:
- Random shuffling and dealing of cards.
- Evaluation of Poker hands (Straight Flush, Four of a Kind, Full House, etc.).
- Leaderboard tracking player performance.

File Handling:
- Player data (names, statistics) saved in CSV files.

## Build Instructions

**Dependencies:**
- C++ compiler supporting C++11 or later (tested with g++ 14.1.0).
- SDL2, SDL2_image, SDL2_mixer, SDL2_ttf libraries.

**Compile Command Example:**

```bash
g++ src/main.cpp src/Game.cpp src/Basic.cpp src/FiveStud.cpp src/Card.cpp \
src/Deck.cpp src/Table.cpp src/Player.cpp src/LeaderBoard.cpp \
src/TextureManager.cpp src/Button.cpp src/InputBox.cpp src/TextBox.cpp \
src/FileHandler.cpp -o PokerGame -I include -L lib \
-lSDL2main -lSDL2 -lSDL2_image -lSDL2_mixer -lSDL2_ttf
