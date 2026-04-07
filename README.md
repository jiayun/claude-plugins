# jy-plugins

Personal [Claude Code plugin](https://docs.anthropic.com/en/docs/claude-code/plugins) collection.

## Skills

### `/magi` - MAGI Decision System

Inspired by the MAGI supercomputer from *Neon Genesis Evangelion*. Launches 3 agents in parallel, each representing a different personality of Dr. Naoko Akagi:

| Unit | Persona | Perspective |
|------|---------|-------------|
| MELCHIOR | Scientist | Rationality, technical rigor, correctness |
| BALTHASAR | Mother | User experience, empathy, long-term nurturing |
| CASPER | Woman | ROI, political reality, community perception |

Each agent independently analyzes the topic and casts a vote (approve/reject/abstain), then results are tallied.

**Usage:**

```
/magi Should we mass-adopt AI code review?
/magi 該不該在週五部署
```

## Installation

Add to your Claude Code settings (`~/.claude/settings.json`):

```json
{
  "extraKnownMarketplaces": {
    "jy-plugins": {
      "source": {
        "source": "github",
        "repo": "jiayun/claude-plugins"
      }
    }
  },
  "enabledPlugins": {
    "jy@jy-plugins": true
  }
}
```

## License

MIT
