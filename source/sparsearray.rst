sparsearray.cpp - Implementation of Sparse Array Template

==============================================================

.. contents:: Table of Contents
    :depth: 2
Introduction

The sparsearray.cpp file provides the implementation for the sparse_array template class, a key component designed to efficiently store and manage components in the game engine.
Implementation Details

sparse_array Template Class
^^^^^^^^^^^^^^^^^^^^^^^^^^^

    Purpose: Implements a sparse array data structure to manage game components efficiently.
    Template Parameters:
        Component: The type of elements stored in the array.
        Allocator: The allocator to use for memory management (default: std::allocator<Component>).

Key Methods and Operators
^^^^^^^^^^^^^^^^^^^^^^^^^

    Constructors and Destructor: Default, copy, and move constructors, along with a destructor for managing the array.
    Copy and Move Assignment Operators: Handles the assignment of sparse arrays.
    Element Access Operators ([]): Provides access to elements in the array.
    Iterators: Methods like begin(), end(), cbegin(), and cend() for iterator support.
    size() Method: Returns the number of elements in the array.
    Modifiers:
        insert_at(): Inserts a component at a specified position.
        emplace_at(): Constructs an element in-place at a specified position.
        erase(): Removes an element from a specified position.
        clean_sparse_array(): Cleans up the array, removing empty or default elements.
    has_component() Method: Checks if a component exists at a specified position.
    get_index() Method: Finds the index of a given component value.

Conclusion

The sparsearray.cpp file is essential for efficient component management in the game engine. It provides a flexible and performant way to store and access game components, crucial for the dynamic aspects of game development in the R-Type project.