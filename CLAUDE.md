# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build/Test Commands
- Install dependencies: `bundle install`
- Run all tests: `bundle exec rake` or `bundle exec rspec`
- Run a specific test: `bundle exec rspec spec/path/to/specific_test_spec.rb:LINE_NUM`
- Run dummy app tests for specific Rails version: `act -W .github/workflows/test.yml -P ubuntu-latest=ghcr.io/catthehacker/ubuntu:act-latest --no-cache-server --matrix rails-version:7`

## Code Style Guidelines
- Indentation: 2 spaces
- Naming: snake_case for files/methods, CamelCase for classes/modules, ALL_CAPS for constants
- Method organization: group public, protected, and private methods with appropriate keywords
- Use keyword arguments for method parameters when appropriate
- Tests: RSpec with describe/context blocks, and let/before for setup
- Error handling: Custom error classes inherit from StandardError
- Avoid modifying Rails config settings in the lib code (leave it to gem users)
- Follow Ruby documentation conventions (yard/rdoc style)
- Use I18n for error messages and notifications
- Ensure compatibility with multiple Rails versions (6.0+)