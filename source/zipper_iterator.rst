zipper_iterator.hpp - Zipper Iterator for Container Synchronization

=======================================================================

.. contents:: Table of Contents
    :depth: 2
Introduction

The zipper_iterator.hpp file defines the zipper_iterator template class, a sophisticated iterator tool designed to iterate over multiple containers in a synchronized manner. It is particularly useful in scenarios where elements from different containers need to be processed together.
Template Class Design

zipper_iterator
^^^^^^^^^^^^^^^^

    Purpose: Allows synchronized iteration over multiple containers.
    Template Parameters: Containers... - The types of containers to be zipped together.
    Type Definitions:
        value_type: A std::tuple holding references to the elements of the containers.
        reference: The reference type for value_type.
        pointer: Void, as raw pointers are not used.
        difference_type: Typically std::ptrdiff_t, for pointer arithmetic.
        iterator_category: Set to std::input_iterator_tag.
        iterator_tuple: A tuple of iterators, one for each container.

Key Methods and Operators
^^^^^^^^^^^^^^^^^^^^^^^^^

    Constructors: Standard and copy constructors for initializing the iterator.
    Increment Operators (++): Prefix and postfix increment operators to advance the iterator.
    Dereference Operators (*, ->): To access the current element(s) in the zipped containers.
    Equality/Inequality Comparisons (==, !=): For comparing the positions of two zipper_iterator instances.

Private Member Functions
^^^^^^^^^^^^^^^^^^^^^^^^

    incr_all(std::index_sequence<Is...>): Increments all iterators in the tuple.
    to_value(std::index_sequence<Is...>): Retrieves a tuple of the current elements from each container.

Conclusion

The zipper_iterator template class is a powerful utility in the C++ toolkit, enabling synchronized traversal over multiple containers. Its ability to "zip" together several containers into a single iterator interface makes it ideal for complex data manipulation and parallel processing tasks in the R-Type project.
