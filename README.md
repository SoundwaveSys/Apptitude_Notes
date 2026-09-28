## Problem

Currently, if the Ollama server is not running or cannot be reached,
GWEN may return a generic connection error.

## Expected behavior

GWEN should detect when the Ollama server is unavailable and display
a clear error message explaining:

- Ollama is not running or cannot be reached
- The configured Ollama URL
- How the user can start Ollama

## Example

Instead of showing a raw connection/HTTP error, show something like:

"Unable to connect to Ollama at http://localhost:11434.
Please make sure Ollama is running and try again."

## Acceptance criteria

- [ ] Detect Ollama connection failures
- [ ] Return a user-friendly error message
- [ ] Include the configured Ollama URL
- [ ] Do not expose sensitive environment variables
- [ ] Keep the existing successful Ollama workflow unchanged
