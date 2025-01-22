# Webserv

**Webserv** is a custom HTTP server built in C++ 98. This project demonstrates a deep understanding of the HTTP protocol and server-client communication. It serves as a foundation for understanding the mechanics of web servers, including handling requests, responses, and static content delivery.

## Features

- **HTTP Methods**: Supports `GET`, `POST`, and `DELETE` methods.
- **Non-blocking I/O**: Implements efficient I/O operations using `poll()` or equivalent.
- **Configuration File**: Fully customizable server settings via a configuration file.
- **Error Handling**: Provides default error pages for HTTP error responses.
- **Static Website Hosting**: Serves static files and directories.
- **File Uploads**: Allows clients to upload files to the server.
- **Multiple Ports**: Can listen and respond to multiple ports simultaneously.
- **CGI Execution**: Executes CGI scripts based on file extensions (e.g., `.php`).
- **Stress Tested**: Designed to handle high traffic without crashing.

## Requirements

- C++ 98 standard
- External functions used:
  - `execve`, `dup`, `dup2`, `pipe`, `strerror`, `socket`, `accept`, `listen`, `send`, `recv`, and others.
- Compatible with most modern web browsers.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/username/webserv.git
   cd webserv
   ```

2. Compile the project:
   ```bash
   make
   ```

3. Run the server:
   ```bash
   ./webserv [configuration file]
   ```
   If no configuration file is provided, the server uses a default path.

## Configuration

The server is configured via a file that allows you to:
- Set ports and hosts for multiple servers.
- Define server names and default error pages.
- Limit client body size.
- Configure routes with specific rules:
  - Accepted HTTP methods
  - Directory listing
  - Default files for directories
  - File upload destinations
  - CGI execution

Refer to the sample configuration file provided in the repository for details.

## Bonus Features (Optional)

- Cookie and session management.
- Support for multiple CGI implementations.

## Project Details

This project adheres to strict rules to ensure stability and compatibility:
- Non-blocking operations for all client-server interactions.
- Fully resilient design to handle unexpected crashes or memory issues.
- Developed without using external or Boost libraries.

## Acknowledgments

This project is inspired by the HTTP server functionality of NGINX. Testing was performed using various tools and browsers to ensure compliance and reliability.
