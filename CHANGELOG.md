# Changelog

All notable changes to rust-skills will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-01-16

### Added

#### Core Infrastructure
- Initial release of rust-skills Claude plugin
- 15 meta-question skills (m01-m15) for Rust learning
- rust-router for intelligent skill routing
- rust-learner for crate and version information

#### Skills
- **m01-ownership**: Memory ownership and lifetimes
- **m02-resource**: Resource management (Box, Rc, Arc)
- **m03-mutability**: Mutability patterns
- **m04-zero-cost**: Zero-cost abstractions
- **m05-type-driven**: Type-driven design
- **m06-error-handling**: Error handling patterns
- **m07-concurrency**: Concurrency and async
- **m08-safety**: Safety abstractions
- **m09-domain**: Domain modeling
- **m10-performance**: Performance optimization
- **m11-ecosystem**: Ecosystem integration
- **m12-lifecycle**: Resource lifecycle
- **m13-domain-error**: Domain error handling
- **m14-mental-model**: Mental model construction
- **m15-anti-pattern**: Anti-pattern recognition

#### unsafe-checker Skill
- 47 unsafe rules organized by category
- Checklists for writing and reviewing unsafe code
- FFI best practices and patterns
- Examples for safe abstractions

#### coding-guidelines Skill
- Compressed P rules by category (~80 core rules)
- G rules summary (g-compressed.md)
- Clippy lint mapping index

#### Agents
- crate-researcher: Fetch crate info from lib.rs/crates.io
- rust-changelog: Fetch Rust version changelog
- docs-researcher: Fetch API documentation
- clippy-researcher: Fetch Clippy lint information
- browser-fetcher: Generic web content fetching

#### Commands
- /guideline: Query coding guidelines
- /guideline --clippy: Map Clippy lints to rules
- /unsafe-check: Check file for unsafe issues
- /unsafe-review: Interactive unsafe code review

#### Deep Dive Content
- Common error patterns and fixes
- Lifetime patterns guide
- Async patterns guide
- Thread-based concurrency patterns
- Performance optimization guide
- Mental model construction guide
- Anti-pattern recognition guide
- Language comparison documents

#### Code Templates
- Error handling templates (thiserror, anyhow)
- Concurrency templates (worker-pool, async-task)
- FFI templates (safe-wrapper)

#### Testing
- Test scenarios for all major skills
- Validation script for skill configuration
- Agent integration test scenarios

#### Caching
- Agent result caching system
- Configurable TTL per category
- Cache management utilities

### Technical Details
- Skills use YAML frontmatter for triggers
- Agents use haiku model for efficiency
- Routing based on keywords and error codes
- Chinese language triggers supported

## [Unreleased]

### Planned
- Domain skills expansion (fintech, cloud-native, ML)
- More code templates
- Index generation tools
- Additional test coverage
