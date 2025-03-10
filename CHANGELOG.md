# Changelog

## [v0.0.30]
- support deepseek api reasoning model's reasoning content

## [v0.0.29]
- remove Anthropic from /models since it doesn't work yet


## [v0.0.28]
- fix max_tokens calculation
- add dynamic reasoning effort up to the defined max in /config or /model. You can say things like "megathink" and it'll be set to high. This follows claude-code and you can check out `src/utils/thinking.ts` for the details.

## [v0.0.27]
- fix lsTool to not show the safety warning to the user
- fix tool description truncation for openai models

## [v0.0.26]
- buffer the rawdog stream

## [v0.0.25]
- Rawdog the completion call because everyone sucks

## [v0.0.24]
- Add thinking and reasoning blocks to the assistant message

## [v0.0.23]
- Remove the call to updateTerminalTitle in REPL.tsx

## [v0.0.22]
- Get API key from env if available
- Add proxy support

## [v0.0.21]
- Fix #20
- Fix max token input field and reasoning effort in /config

## [v0.0.20]
- Fixed ! bash mode
- Fixed #3 An assistant message with 'tool_calls' must be followed by a tool result error
- Removed AutoUpdater component

## [v0.0.19]
- Added support for LLM servers that don't include `usage` or token counts in their responses (e.g. LM Studio)
  - Modified query handling to work with servers that don't return token usage metrics
  - Improved compatibility with third-party LLM servers
- Updated issue templates for better bug reporting
- Updated README.md with improved documentation

## [v0.0.18]
- Implemented `/bug` command for submitting feedback directly from the CLI
  - Created Bug component to handle feedback submission workflow
  - Integrated with GitHub issue reporting
- Updated issue templates for more structured bug reporting

## [v0.0.17]
- Fixed model selection and configuration bugs
  - Resolved issues with model detection and selection
  - Fixed configuration persistence issues

## [v0.0.16]
- Added support for OpenAI's `reasoning_effort` parameter
  - Updated models.ts to include `supports_reasoning_effort` flag for compatible models
  - Added configuration screen for max tokens and reasoning effort
  - Modified the claude.ts service to respect these new parameters
- Updated model config handling in API calls
- Fixed various bugs related to model configuration and token usage

## [v0.0.15]
- Updated README documentation with clearer usage instructions

## [v0.0.14]
- Added single release workflow that handles version bump, build, and publish
  - Streamlined the release process with automated versioning
  - Improved CI/CD pipeline
- Updated README with new single release workflow information

## [v0.0.13]
- Fixed version-bump workflow to properly trigger build and publish processes

## [v0.0.12]
- Fixed build process and dependency issues
- Improved build script reliability

## [v0.0.11]
- Fixed npm-publish workflow to install Bun for proper builds
- Improved deployment pipeline configuration

## [v0.0.10]
- Fixed npm-publish.yml workflow file for more reliable deployments

## [v0.0.9]
- Initial tagged release
- Basic CLI functionality established
