B5 - Advanced C++
=================

.. contents:: Table of Contents
   :depth: 2

Introduction
------------

The **B-CPP-500 R-Type** project is an advanced C++ project that involves developing a networked video game based on the legacy game R-Type. This document serves as the primary source of information and guidelines for the project.

.. note::
   This project will introduce you to networked video game development and advanced development techniques in C++.

Project Overview
----------------

- **Game Type**: Horizontal Shmup (Shoot'em'up)
- **Languages**: C++
- **Tools**: CMake, Optional Package Manager
- **Binary Names**: ``r-type_server``, ``r-type_client``

Software Engineering Requirements
---------------------------------

- **Build System**: The project must use CMake. No Makefiles are allowed.
- **Dependencies**: The project must be self-contained regarding its dependencies.
- **Cross-Platform**: Must build and run on both Windows (MSVC) and Linux (GCC).

Documentation Requirements
--------------------------

.. highlight:: restructuredtext

- **Language**: All documentation must be written in English.
- **Formats**: Use modern documentation delivery methods like Markdown or reStructuredText.

Part 1: Core Game Development
-----------------------------

- **Objective**: Develop the core architecture of the game and a working prototype.
- **Networking**: The game must demonstrate a networked structure with a clear server-client model.

.. code-block:: cpp

   int main() {
       // Example code snippet
   }

Part 2: Advanced Development
----------------------------

- **Advanced Architecture**: Expand the software architecture, possibly creating a separate game engine.
- **Networking**: Enhance the networking capabilities for efficiency and reliability.
- **Gameplay**: Improve gameplay with additional content and better tools for content creation.

Conclusion
----------

The B5 - Advanced C++ R-Type project is a comprehensive undertaking that will test your skills in software development, particularly in the context of game development. Embrace the challenges and use this opportunity to enhance your understanding of C++ and game design.

.. admonition:: Note
   Remember to update and refine your documentation as the project evolves.
