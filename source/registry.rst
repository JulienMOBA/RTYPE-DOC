registry.hpp - Component Registry for Game Development

========================================================
Contents

    Introduction
    File Description
    Key Functions
    Usage Examples
    Included Libraries and Their Purposes

Introduction
^^^^^^^^^^^^
The registry.hpp file is a core part of the B-CPP-500 R-Type project. It is designed for efficient management of game entities and their components within the game's architecture, especially in a networked environment.
File Description

    Purpose: To provide a central registry system for managing game entities and components.
    Primary Role: Handling creation, retrieval, and management of game components and entities.

Key Functions

    register_component<Component>():
        Purpose: Registers a new component type in the registry.
        Parameters: Template parameter Component - Type of the component to register.
        Return: Reference to the sparse_array of the registered component.

    get_components<Component>():
        Purpose: Retrieves the array of components of a specific type.
        Parameters: Template parameter Component - Type of the component to retrieve.
        Return: Reference to the sparse_array of the requested component.

    spawn_entity():
        Purpose: Creates a new game entity.
        Return: entity_t representing the unique ID of the new entity.

    kill_entity(entity_t const& e):
        Purpose: Marks an entity for removal from the game.
        Parameters: e - The entity to be removed.

    add_component<Component>(entity_t const& to, Component&& component):
        Purpose: Adds a component to a specified entity.
        Parameters: to - Entity ID to add the component to; component - The component to be added.
        Return: Reference to the added component.

    run_systems():
        Purpose: Executes all registered systems in the registry.
        Details: Systems are functions that operate on components and entities.

Usage Examples

cpp

registry myRegistry;
auto& positionComponents = myRegistry.register_component<PositionComponent>();
entity_t playerEntity = myRegistry.spawn_entity();
myRegistry.add_component(playerEntity, PositionComponent{0, 0});

Included Libraries and Their Purposes

    <any>: For storing any type of component in a type-safe way.
    <cstdint>: For standard integer type definitions.
    <functional>: For handling function objects and lambda expressions.
    <stdexcept>: For exception handling.
    <typeindex>: For managing type information at runtime.
    <unordered_map>: For efficient storage and retrieval of components.
    <vector>: For dynamic array management, used in storing entities and components.

Conclusion

The registry.hpp file is fundamental in managing the dynamic aspects of game entities and their behaviors. It enables a modular and efficient approach to building and managing game components, crucial for the development of the B-CPP-500 R-Type project.