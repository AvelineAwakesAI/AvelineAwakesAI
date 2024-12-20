# AI AGENT AVELINE

![banner]()

Aveline is a AI agent developed with rig, designed to autonomously interact on X. She expresses a unique and consistent personality while crafting poetry, composing music, creating art, and more.

Follow our AI agent: (https://x.com/AvelineAwakesAI)


## Overview

This project introduces an AI-driven social media agent capable of autonomous engagement on platforms, maintaining a cohesive personality and interacting naturally. Built with Rust for speed and reliability, it leverages the rig framework to enable robust AI functionality.

## Core Features

### Character-Based Design
- Implements a structured framework to ensure the agent’s personality traits are consistently portrayed
- Offers adjustable writing styles and topic preferences for tailored content
- Creates dynamic responses aligned with the character’s unique profile

### Autonomous Social Engagement
- Produces original, contextually appropriate posts
- Responds intelligently to mentions and conversations
- Prioritizes engagements with a smart filtering system
- Sustains smooth and natural conversation flows

### Enhanced Memory Capabilities
- Maintains a persistent log of interaction history
- Generates replies that account for prior context
- Tracks user relationships to enhance future interactions

### Social Media Platform Integration
- Built-in rate limiting and post scheduling functionality
- Uses random delays to simulate human-like posting habits
- Fully supports Twitter API v2 for seamless integration

### Flexible and Modular Design
- Clearly separates core logic from integrations
- Expandable framework for character trait definitions
- Modular provider system for enhanced adaptability
- Optimized memory management for efficient operation

## System Requirements

- Rust (latest stable version)
- API Keys:
  - Anthropic Claude API access
  - Twitter API v2 credentials (OAuth 1.0a)

## Installation

1. Create a `.env` file with required credentials:
ANTHROPIC_API_KEY=your_api_key
TWITTER_CONSUMER_KEY=your_key
TWITTER_CONSUMER_SECRET=your_secret
TWITTER_ACCESS_TOKEN=your_token
TWITTER_ACCESS_TOKEN_SECRET=your_token_secret
CHARACTER_NAME=your_character_name

2. Configure your character:
   - Create a new directory: `characters/{CHARACTER_NAME}/`
   - Add character definition in `character.json`

## Character Configuration

Characters are defined using a structured JSON format:

{
  "instructions": {
    "base": "Base character instructions",
    "suffix": "Additional instructions"
  },
  "adjectives": ["trait1", "trait2"],
  "bio": {
    "headline": "Character headline",
    "key_traits": ["trait1", "trait2"]
  },
  "lore": ["background1", "background2"],
  "styles": ["style1", "style2"],
  "topics": ["topic1", "topic2"],
  "post_style_examples": ["example1", "example2"]
}

## Usage

Run the agent:
cargo run

## Project Layout

aveline/
├── src/
│   ├── core/           # Core agent functionality
│   ├── characteristics/ # Character trait implementations
│   ├── providers/      # External service integrations
│   └── memory/         # Persistence layer
├── characters/         # Character definitions
└── tests/             # Test suite

## Key Dependencies

- [rig](https://github.com/0xPlaygrounds/rig) - AI agent framework
- `twitter-v2` - Twitter API client
- `tokio` - Async runtime
- `serde` - Serialization/deserialization
- `anyhow` - Simplified error handling in Rust


## Special Thanks

- [rig](https://github.com/0xPlaygrounds/rig) team for the AI agent framework
- Appreciation to contributors and maintainers for their support in this project.

## Support

For questions and support, please open an issue in the GitHub repository.
