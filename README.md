# technical-writer-plugin

This Claude Code plugin helps you write more effective technical documentation.

## Usage

You may use this plugin to assist in writing a variety of technical documents and artifacts.

### Code comments

#### Skill - `/technical-writer:comment`

This skill provides instructions for writing effective interface and implementation comments per the recommendations contained in John Ousterhout's *A Philosophy of Software Design*.

You can either invoke the skill directly or instruct Claude to use the provided subagent.

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

Note: you'll need to use `technical-writer:comment` if you experience any conflicts between plugins.

#### Agent - `technical-writer:commentator`

Sometimes, it makes sense to spin up a subagent (or multiple subagents in parallel) to add interface and implementation comments. Using the subagent will invoke the skill while keeping your context window clean.

Conversationally instruct Claude to use the commentator subagent to document code:

```
Use the commentator agent to add comments for each of the controllers
```

Note: you'll need to use `technical-writer:commentator` if you experience any conflicts between plugins.
