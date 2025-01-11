# AniList CLI Project Guide

## Overview

This document provides a comprehensive guide for building an AniList API-based CLI tool using C. It emphasizes deepening your understanding of advanced C concepts while developing a practical project.

---

## Key Topics to Explore

### 1. Advanced C Concepts

- **Dynamic Memory Management**: Efficient use of `malloc`, `calloc`, `realloc`, and `free`.
- **Pointers and Pointer Arithmetic**: Master complex data structures and low-level manipulation.
  - [Pointers and Arrays Tutorial](https://github.com/jflaherty/ptrtut13)
- **File I/O Operations**: Efficient data storage and retrieval.
- **Function Pointers and Callbacks**: Useful for abstraction in CLI commands.
- **Multithreading (Optional)**: Use libraries like `pthread` for concurrent request handling.

### 2. Networking and GraphQL API Integration

- **HTTP Requests with `libcurl`**: Essential for making GraphQL queries to the AniList API.
- **GraphQL Queries**: Write and format GraphQL queries as JSON payloads for API communication.
- **Parsing JSON in C**: Use libraries like `cJSON` or `jansson` to parse responses from the AniList API effectively.

#### Example GraphQL Request Structure

A typical AniList query looks like:

```json
{
  "query": "query { Media(id: 1, type: ANIME) { title { romaji english } } }"
}
```

You can send this as a POST request to `https://graphql.anilist.co`

### 3. CLI Design Patterns

- Build an intuitive and extendable interface.
- Use command parsing frameworks or build a minimalist custom solution.
- Consider argument parsing with libraries such as `argp` or custom-built solutions.

### 4. Error Handling and Robustness

- Implement graceful error handling to ensure a stable CLI tool.
- Use `errno`, custom error codes, and logging for better diagnostics.

---

## Recommended Resources

### Books

- **"C Programming: A Modern Approach" by K. N. King**
- **"Expert C Programming: Deep C Secrets" by Peter van der Linden**
- **"Advanced Programming in the UNIX Environment" by W. Richard Stevens**
- **"Computer Systems: A Programmer's Perspective" by Bryant and O'Hallaron**

### Online Resources

- [Beej’s Guide to Network Programming](http://beej.us/guide/bgnet/)
- [Linux Man Pages](https://man7.org/linux/man-pages/)
- [Pointers and Arrays Tutorial](https://github.com/jflaherty/ptrtut13)
- Explore GitHub for similar open-source C projects to learn real-world implementations.

---

## Project Enhancement Ideas

- **User Authentication**: Add OAuth2 for secure API access.
- **Caching System**: Store recent requests locally to reduce API calls.
- **Multithreaded Fetching**: Speed up data retrieval using concurrent requests.
- **User Preferences and Config Management**: Allow persistent user settings.
- **Custom Output Formatting**: Parse JSON and display tables using libraries like `ncurses`.

---

## Suggested Learning Path

1. **Core Book Learning**:
   - Follow "C Programming: A Modern Approach" to reinforce your C fundamentals.
   - Supplement with "Expert C Programming" for advanced insights.

2. **API Integration**:
   - Learn and implement HTTP requests using `libcurl`.
   - Handle API responses with JSON parsing libraries.

3. **CLI Development**:
   - Start by creating a basic tool that handles user input and displays mock data.
   - Gradually implement API calls and improve error handling.

4. **Enhancement and Optimization**:
   - Add concurrency, caching, and configuration management as you progress.
