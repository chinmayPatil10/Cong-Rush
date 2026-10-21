# Script reference

This list was recovered from the metadata of `Assembly-CSharp.dll` in the shipped Android build. It shows every class, its field and method counts, and notable members. Method bodies weren't decompiled.

## Gameplay

| Class | Fields | Methods | Notable members |
|---|---|---|---|
| `SimplePlatFormController` | 9 | 5 | `facingRight`, `jump`, `moveForce`, `maxSpeed`, `jumpForce`, `groundCheck`, `grounded`, `Flip()`, `FixedUpdate()` |
| `PlayerController` | 13 | 6 | `doubleJump`, `isGrounded`, `whatIsGround`, `rb2d`, `m_Anim`, `OnTriggerEnter2D()` |
| `PlayerController_m` | 12 | 6 | Variant of `PlayerController` used in some levels |
| `CameraController` / `CameraController_m` | 3 | 3 | Camera follow |
| `PlatformFall` | 2 | 4 | `Falldelay`, `Fall()`: drops after the player lands |
| `HitVelDetection` | 0 | 4 | Collision velocity checks |

## Coins, score and timer

| Class | Fields | Methods | Notable members |
|---|---|---|---|
| `SpawnManager` | 7 | 3 | Platform spawner: `maxPlatforms`, `platform`, `horizontalMin/Max`, `verticalMin/Max`, `originPosition`, `Spawn()` |
| `SpawnCoins` | 2 | 3 | `coinSpawns`, `coin` |
| `SpawnCoin` | 2 | 3 | `coinsSpawns`, `coin` |
| `Coin` | 1 | 4 | `scoreValue`, `OnTriggerEnter2D()` |
| `ponits` | 2 | 3 | `score`, `text`: score HUD |
| `remaining` | 2 | 3 | Coins-remaining HUD |
| `CountDownTimer` | 2 | 2 | `timeLeft`, `text` |

## Scene / menu flow

| Class | Fields | Methods | Notable members |
|---|---|---|---|
| `GameOver` | 0 | 3 | Game Over screen buttons |
| `Win` / `WinMenu` | 0 | 3 | Loads the `WIN` scene / win menu buttons |
| `Nextlevel` | 0 | 3 | Level navigation (`ChangeScene(sceneName)`) |
| `Reset` | 0 | 4 | Reset / retry |

## Background / effects

| Class | Fields | Methods | Notable members |
|---|---|---|---|
| `Instantiation` | 1 | 3 | Spawns clouds |
| `DestroyCloud` / `DestroyCloud_m` | 0 | 3–4 | Destroys off-screen clouds |
| `ArmRotation` | 1 | 2 | `rotationOffset`: arm/aim rotation (part of the shooting template) |

## Unused template code (shooting kit)

A gun-controller asset was imported into the project but never used in any level:

`gun_controller` (45 fields, 99 methods), `example_gun_controller`, `mock_aim_controller`, `mock_player_controller`, `bullet_trail`, `muzzle_flash`. It covers fire rate, burst/auto modes, recoil, accuracy by stance, ammo/magazines and reload.

## Third-party utilities

`wHiteRabbiT.Unity.Extensions` (`VectorExtensions`, `QuaternionExtensions`, `ColorExtensions`), `wHiteRabbiT.Unity.UI.GUIHelper`, `wHiteRabbiT.Unity.Util.Logo`.

## Scenes (build order)

`Start Screen`, `levelselector`, `24k magic`, `Black Beatles`, `Rockabye`, `cheap thrills`, `closer`, `coldwater`, `hymm`, `in the name of love`, `let me love you`, `starboy`, `gameover`, `WIN`
