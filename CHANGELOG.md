# Changelog

All notable changes to DocBlock AI will be documented in this file.

## [1.3.2] - 2026-11-06

### Changed

- Added author information to the extension manifest

## [1.3.1] - 2026-11-06

### Changed

- Extension is now bundled with esbuild: smaller package (8 files instead of ~1800) and faster startup
- Added MIT license

## [1.3.0] - 2026-11-06

### Added

- Claude Sonnet 5.5, Opus 5.5 and Fable 5.1; Claude Sonnet 5.5 is the new default
- GPT-6.1 Terra, GPT-6.1 Sol, GPT-5.5 and GPT-5.4 mini; GPT-6.1 Terra is the new OpenAI default
- Request timeouts so generation no longer hangs on network issues

### Removed

- Retired OpenAI models (gpt-4-turbo, gpt-3.5-turbo, gpt-4o) and gpt-4; settings using them switch to GPT-6.1 Terra

### Fixed

- Empty results with Claude models that think before answering; Claude refusals now show a clear message

## [1.2.4] - 2026-04-23

### Fixed

- Generated comment opening normalized: `/***...` is now always corrected to `/**`

## [1.2.3] - 2026-04-23

### Fixed

- Generated comment now inherits the indentation of the selected code
- Blank lines between tag groups (@param, @return, @throws) to match standard PHPDoc/JSDoc formatting

## [1.2.2] - 2026-04-23

### Changed

- Description now generates 2–3 sentences with line wrapping at 80 characters

## [1.2.1] - 2026-04-23

### Added

- Support for documenting classes, interfaces, variables, constants, and properties in all 9 languages
- Anthropic Claude provider (Haiku 4.5 / Sonnet 4.6 / Opus 4.7) with `DocBlock AI: Set Claude API Key` command

## [1.2.0] - 2026-04-23

### Fixed

- Error "TextEditor#edit not possible on closed editors" when the file is closed during generation
- Generated comment incorrectly starting with `/ **` instead of `/**`

### Changed

- Shorter documentation output: one concise summary sentence instead of a two-paragraph description

## [1.1.0] - 2026-04-23

### Added

- Support for 9 programming languages: PHP, JavaScript, TypeScript, Python, Java, C#, Go, Ruby, Rust
- Correct documentation format per language: PHPDoc, JSDoc, TSDoc, Google docstring, Javadoc, XML doc, GoDoc, YARD, Rustdoc
- Two AI providers: OpenAI GPT and GitHub Copilot
- OpenAI model selection: GPT-3.5 Turbo, GPT-4, GPT-4 Turbo, GPT-4o
- Documentation text in 10 human languages
- Right-click context menu: "DocBlock AI: Generate Documentation"
- Progress notification with cancellation support
