# comments-plugin

This Claude Code plugin helps you write more effective code comments per the recommendations contained in John Ousterhout's *A Philosophy of Software Design*.

## Usage

You can either invoke the skill directly or instruct Claude to use the provided subagent. Using the subagent will invoke the skill while keeping your context window clean.

### Skill

Invoke the comment skill for a specific file:

```
/comment path/to/file.rb
```

Invoke the comment skill for a class/module:

```
/comment User
```

Invoke the comment skill for the broader codebase:

```
/comment
```

Conversationally invoke the comment skill:

```
Use the comment skill to add comments for each of the controllers
```

Note: you'll need to use `comments-plugin:comment` if you experience any conflicts between plugins.

### Agent

Conversationally instruct Claude to use the commentator subagent to document code:

```
Use the commentator agent to add comments for each of the controllers
```

Note: you'll need to use `comments-plugin:commentator` if you experience any conflicts between plugins.
