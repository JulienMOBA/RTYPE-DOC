components.hpp - Game Component Structures

===================================================

.. contents:: Table of Contents
    :depth: 2

Introduction

The components.hpp file is a crucial part of the game's architecture, defining various structures representing different game components. These components are used to assign properties and behaviors to game entities.
Structures Overview

Position
^^^^^^^^

    Purpose: Represents an entity's position and velocity in the game world.
    Attributes: x, y for position; vx, vy for velocity.

Drawable
^^^^^^^^

    Purpose: To hold a drawable sprite using the SFML library.
    Attributes: sf::Sprite sprite.

Clickable
^^^^^^^^^

    Purpose: Defines clickable UI elements like buttons.
    Attributes: An enumeration buttonType with values like startGame, options, leaveGame.

Sound
^^^^^

    Purpose: Manages sound properties for an entity.
    Attributes: soundLocation for file path, volume (0 to 100), and loop as a boolean.

Controllable
^^^^^^^^^^^^

    Purpose: Assigns keyboard controls to an entity.
    Attributes: sf::Keyboard::Key for up, down, left, right, escape.

Speed
^^^^^

    Purpose: Specifies the speed of an entity.
    Attributes: speed as a float.

Hitable
^^^^^^^

    Purpose: Defines a hitbox for collision detection.
    Attributes: x, y, width, height for hitbox dimensions.

Health
^^^^^^

    Purpose: Manages health-related properties.
    Attributes: maxHealth, health.

Weaponized
^^^^^^^^^^

    Purpose: Assigns weapon properties to an entity.
    Attributes: Enumeration weapon, weaponLevel, nbProjectile.

Damage
^^^^^^

    Purpose: Represents the damage capability of an entity.
    Attributes: dmg as a float.

Item
^^^^

    Purpose: Represents items that can be collected for upgrades.
    Attributes: Enumeration items with types like heal, maxHealth, etc.

Score
^^^^^

    Purpose: Holds the game score.
    Attributes: score as a float.

Life
^^^^

    Purpose: Represents the number of lives an entity has.
    Attributes: nbLives as an integer.

Area
^^^^

    Purpose: Defines an area of effect.
    Attributes: area as a float.

Text
^^^^

    Purpose: Manages text properties for display.
    Attributes: text, size in pixels, fontLocation, sf::Color color.

Conclusion

The components.hpp file defines a set of structures essential for various aspects of game functionality, from controlling entity behavior to managing UI elements. Proper understanding and usage of these components are key to effective game development in the R-Type project.