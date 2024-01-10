scene_manager.hpp - Scene Management for Game Development

=============================================================

.. contents:: Table of Contents
    :depth: 2
Introduction

scene_manager.hpp is a key component in the game's architecture, responsible for managing different scenes within the game. It includes classes and structures for handling various elements like buttons, interactive elements, and static elements in a scene.
Structures and Classes Overview

Button
^^^^^^

    Purpose: Represents a UI button in a scene.
    Attributes: id, texture_path, coordinates x, y, text, font_path, color, type, size, scale.

InteractiveElement
^^^^^^^^^^^^^^^^^^

    Purpose: Defines interactive elements within a scene.
    Attributes: id, type, src (source path), x, y, dimensions width, height.

StaticElement
^^^^^^^^^^^^^

    Purpose: Represents static text or images in a scene.
    Attributes: id, type, content, x, y, font_size, color.

Screen
^^^^^^

    Purpose: Represents a complete scene with various elements and an ECS (Entity Component System).
    Attributes: name, buttons, interactive_elements, static_elements, ecs (registry object).

SceneManager Class
^^^^^^^^^^^^^^^^^^

    Purpose: Manages different scenes in the game, including scene creation, switching, and running scene systems.
    Key Methods:
        create_scene(): Creates a new scene and returns its index.
        switch_scene(int scene_index): Switches to the specified scene.
        get_current_scene(): Returns a reference to the current scene's registry.
        run_current_scene_systems(): Executes systems for the current scene.

Conclusion

The scene_manager.hpp file is instrumental in managing various scenes in the game, allowing for a dynamic and interactive game environment. It is essential for developers to understand and utilize this file effectively for efficient scene management in the R-Type project.