zipper.hpp - Zipper Class for Synchronized Container Iteration

==================================================================

.. contents:: Table of Contents
    :depth: 2
Introduction

The zipper.hpp file introduces the zipper template class, designed to facilitate the synchronized iteration over multiple containers. It utilizes the zipper_iterator class to create a seamless interface for handling multiple containers as if they were a single collection.
Template Class Design

zipper
^^^^^^

    Purpose: Creates a synchronized iterator interface for multiple containers.
    Template Parameters: Containers... - The types of containers to be zipped together.
    Type Definitions:
        iterator: Defined as zipper_iterator<Containers...>.
        iterator_tuple: A tuple of iterators, one for each container.

Key Methods
^^^^^^^^^^^

    Constructor: Initializes the zipper with references to the containers. Computes the size and end iterators for the zipped iteration.
    begin() Method: Returns an iterator to the beginning of the zipped containers.
    end() Method: Returns an iterator to the end of the zipped containers.

Private Member Functions
^^^^^^^^^^^^^^^^^^^^^^^^

    _compute_size(Containers&... containers): Computes the maximum size among the provided containers.
    _compute_end(Containers&... containers): Creates an iterator tuple pointing to the end of each container.

Conclusion

The zipper class offers an elegant solution for iterating over multiple containers simultaneously, enhancing the ability to perform complex operations that require data from multiple sources. Its integration with the zipper_iterator class makes it a valuable tool for advanced data manipulation and parallel processing in the R-Type project.