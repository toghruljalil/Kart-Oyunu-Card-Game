# Kart Oyunu Projesi

Short description: A Unity turn-based card battle game where the player fights against the computer using land, air, and sea combat vehicle cards.

## About

This project is a simple 3D/GUI card game built with Unity. The player enters basic game information from the menu, receives a random hand of combat cards, then selects three cards each turn. The computer also chooses three cards, attacks are calculated, destroyed cards give score points, and the game ends when the move limit is reached or one side runs out of cards.

## Gameplay

- The game starts from the `menu` scene.
- The player enters name, ID, move count, and starting level value.
- Both player and computer receive random cards.
- Each turn, the player selects 3 cards.
- The computer randomly selects 3 cards.
- Cards attack each other based on class and bonus damage values.
- Destroyed cards increase the opponent card's level and total score.
- The winner is decided by score, move count, or remaining cards.

## Card Types

- `Ucak`: air card with bonus damage against land.
- `Siha`: air card with bonus damage against land and sea.
- `Obus`: land card with bonus damage against sea.
- `KFS`: land card with bonus damage against air and sea.
- `Firkateyn`: sea card with bonus damage against air.
- `Sida`: sea card with bonus damage against air and land.

## Main Scripts

- `Oyun.cs`: main turn flow, card selection timing, attack calculation, scoring, and end-game checks.
- `Oyuncu.cs`: player/computer score display and computer card selection.
- `KartDagitma.cs`: deals the player's starting cards and card buttons.
- `KartDagitmaOp.cs`: deals the computer's starting cards.
- `ButonlaKartSec.cs`: handles selecting cards from UI buttons.
- `AdAtama.cs`: saves menu input values with `PlayerPrefs`.
- `ObjectParameters.cs`: stores card durability, attack values, class, and level display data.
- `SahneManager.cs`: handles menu/game scene changes and restart/quit actions.

## Requirements

- Unity `2022.3.10f1`
- TextMeshPro package
- Unity UI package

## How To Run

1. Open the project folder in Unity Hub.
2. Use Unity version `2022.3.10f1` or a compatible `2022.3 LTS` version.
3. Open the `Assets/Scenes/menu.unity` scene.
4. Press Play.
5. Enter player information, then start the game.

## Project Scenes

- `Assets/Scenes/menu.unity`: main menu and input screens.
- `Assets/Scenes/oyun.unity`: main card battle gameplay scene.
