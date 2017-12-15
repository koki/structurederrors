# Structured Errors for Go

Errors are great, but we need to know where they happened and why.
This library defines functions and custom error types for annotating errors with additional context.
It's like customizable stacktraces.

The primary error type, `ErrorWithContext`, attaches a stack of context messages to a base error.
When "re-throwing" an error, use `ContextualizeErrorf` or one of the `*ContextErrorf` functions
to push a message onto the context stack. Also included: convenience methods for common errors and contexts.

