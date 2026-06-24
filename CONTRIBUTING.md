# Contributing to Nexphant

First of all, thank you for considering contributing to Nexphant

Nexphant is an experimental high-performance PHP runtime and framework ecosystem focused on async architecture, developer experience, and modern runtime design.

We welcome contributions of all kinds:

* Bug fixes
* Performance improvements
* Documentation
* Benchmarks
* Tests
* Developer tooling
* Runtime experiments
* Ideas and discussions

---

# Philosophy

Nexphant is built around several core principles:

* Performance without sacrificing developer experience
* Clean and modular architecture
* Async-first mindset
* Low overhead abstractions
* Practical experimentation
* Open ecosystem collaboration

We value:

* Clear code
* Small focused PRs
* Honest benchmarks
* Respectful discussions
* Long-term maintainability

---

# Project Structure

```txt
Nexphant/framework      -> framework layer, routing, middleware, lifecycle
Nexphant/server         -> HTTP/WebSocket/SSE server
Nexphant/runtime        -> workers, event loop, fibers, timers
Nexphant/core           -> ownership, context, cancellation
Nexphant/support        -> helpers, config, environment utilities
Nexphant/database       -> pools, drivers, async database layer
Nexphant/queue          -> queue runtime
Nexphant/cache          -> cache abstraction
Nexphant/observability  -> metrics, health, logging
Nexphant/dev            -> hot reload and DX tooling
```

---

# Requirements

Recommended environment:

* PHP 8.3+
* Linux/macOS
* Composer
* Git

Optional extensions:

```txt
pcntl
posix
sockets
apcu
redis
mysqli
pgsql
sqlite3
event
```

---

# Getting Started

Clone the repository:

```bash
git clone https://github.com/Nexphantlabs/Nexphant.git
cd Nexphant
```

Install dependencies:

```bash
composer install
```

Run development server:

```bash
php Nexphant.dev.php
```

---

# Development Guidelines

## Code Style

* Follow PSR-12 where possible
* Prefer explicit naming
* Avoid unnecessary abstractions
* Keep hot paths lightweight
* Avoid hidden allocations in runtime-critical code

---

## Performance Contributions

Performance changes are welcome, but please:

* Include benchmark results
* Explain tradeoffs
* Avoid micro-optimizations without measurable impact
* Keep readability reasonable

Example benchmark tools:

```bash
k6
wrk
ab
```

---

## Pull Request Guidelines

Before opening a PR:

* Ensure code builds correctly
* Run tests if available
* Keep PR scope focused
* Update docs when needed
* Add benchmarks for runtime-related changes

PR title examples:

```txt
feat(runtime): improve timer scheduler
fix(server): resolve websocket memory leak
perf(http): reduce request parsing allocations
docs(core): improve ownership explanation
```

---

# Branch Naming

Recommended branch naming:

```txt
feature/async-pool
fix/socket-leak
perf/router-fastpath
docs/runtime-lifecycle
```

---

# Reporting Issues

When opening issues, please include:

* PHP version
* OS
* Extensions enabled
* Minimal reproduction
* Expected behavior
* Actual behavior

Performance issues should also include:

* Benchmark tool
* Concurrency/VU count
* Hardware information
* Benchmark script if possible

---

# Security

Please do not publicly disclose security vulnerabilities immediately.

Contact:

* [foundation@nexphant.com](mailto:foundation@nexphant.com)

---

# Discussions & Ideas

Experimental ideas are welcome.

This project explores:

* Async runtime architecture
* Fiber orchestration
* Ownership systems
* Event loops
* Resource lifecycle management
* Native runtime integrations

Even unfinished ideas can be valuable discussions.

---

# Community

Be respectful.

We do not tolerate:

* Harassment
* Toxic behavior
* Personal attacks
* Discrimination

Constructive criticism is always welcome.

---

# License

By contributing, you agree that your contributions will be licensed under the project's open-source license.

---

# Special Thanks

Nexphant is inspired by and deeply respects the async and systems ecosystem around PHP and beyond:

* ReactPHP
* Amp
* Workerman
* FrankenPHP
* Swoole
* Swow
* RoadRunner
* OpenSwoole
* Node.js
* Tokio
* Go runtime
* Rust async ecosystem

Open source moves forward because people build together ❤️
