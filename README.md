# Python OOP Assignment

## Overview
This repository contains solutions for two Python Object-Oriented Programming (OOP) assignments:
1. **Custom Class Design** - Implementation of a `Book` class with inheritance
2. **Polymorphism Challenge** - A vehicle hierarchy demonstrating polymorphism

## Assignment 1: Design Your Own Class

### Book Class
The `Book` class models a physical book with the following features:
- **Attributes**: title, author, pages, genre, current page, and private reviews list
- **Methods**:
  - `read(num_pages)`: Updates current page when reading
  - `add_review(review, rating)`: Adds user reviews with ratings (1-5)
  - `get_average_rating()`: Calculates the average rating from all reviews
  - `__str__()`: Returns a formatted string representation of the book

### Ebook Class
The `Ebook` class extends `Book` with digital-specific features:
- **Additional Attributes**: format_type (PDF, EPUB, etc.), file_size, and download status
- **Additional Methods**:
  - `download()`: Marks the ebook as downloaded
  - `change_format(new_format)`: Updates the ebook's format
- **Overridden Methods**:
  - `read(num_pages)`: Checks if the book is downloaded before reading
  - `__str__()`: Extends the parent's string representation with format info

## Activity 2: Polymorphism Challenge

### Vehicle Class Hierarchy
A base `Vehicle` class with three specialized subclasses:

#### Vehicle (Base Class)
- **Attributes**: name, speed
- **Methods**: move(), describe()

#### Car Class
- **Additional Attributes**: fuel_type, wheels
- **Methods**: move() (overridden), honk()

#### Plane Class
- **Additional Attributes**: max_altitude
- **Methods**: move() (overridden), take_off()

#### Boat Class
- **Additional Attributes**: water_type
- **Methods**: move() (overridden), anchor()

### Polymorphism Demonstration
The code demonstrates polymorphism through:
- A `start_journey()` function that works with any vehicle type
- Different implementations of the `move()` method in each vehicle subclass
- A loop that calls the same method on different object types

## Usage Examples

The code includes examples showing how to:
- Create `Book` and `Ebook` objects
- Read books and handle page progression
- Add reviews and calculate ratings
- Download and change formats for ebooks
- Create different vehicle types
- Demonstrate polymorphic behavior

## Key OOP Concepts Demonstrated

- **Encapsulation**: Private attributes (like `__reviews`)
- **Inheritance**: `Ebook` inheriting from `Book`
- **Polymorphism**: Vehicle subclasses implementing the same methods differently
- **Method Overriding**: `read()` in `Ebook`, `move()` in vehicle subclasses
- **Super()**: Calling parent class methods and constructors
