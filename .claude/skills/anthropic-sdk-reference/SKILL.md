---
name: Anthropic SDK Reference
description: Technical reference for Anthropic official repositories including SDKs, tools, and best practices
---

# Anthropic SDK Reference

## Purpose

Provide comprehensive reference to Anthropic official repositories for technical implementation, API integration, SDK usage, and best practices when building AI-powered applications.

## Official Repositories

### Core SDK Repositories

#### 1. anthropic-sdk-python
**URL**: https://github.com/anthropics/anthropic-sdk-python
**Purpose**: Official Python SDK for Claude API
**Use Cases**:
- Backend API integration
- Python-based AI applications
- Batch processing and automation
- Server-side AI features

**Key Features**:
- Streaming responses
- Function calling / Tool use
- Prompt caching
- Vision capabilities
- Batch API support

**Example Usage**:
```python
import anthropic

client = anthropic.Anthropic(api_key="your-api-key")

message = client.messages.create(
    model="claude-opus-4-6",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Hello, Claude"}
    ]
)
print(message.content)
```

---

#### 2. anthropic-sdk-typescript
**URL**: https://github.com/anthropics/anthropic-sdk-typescript
**Purpose**: Official TypeScript/JavaScript SDK for Claude API
**Use Cases**:
- Frontend integration (React, Vue, Angular)
- Node.js backend services
- Full-stack applications
- Real-time AI chat interfaces

**Key Features**:
- Type-safe API calls
- Streaming with async iterators
- Tool use support
- Browser and Node.js compatible

**Example Usage**:
```typescript
import Anthropic from '@anthropic-ai/sdk';

const client = new Anthropic({
  apiKey: process.env.ANTHROPIC_API_KEY,
});

const message = await client.messages.create({
  model: 'claude-sonnet-4-5-20250929',
  max_tokens: 1024,
  messages: [
    { role: 'user', content: 'Hello, Claude' }
  ],
});

console.log(message.content);
```

---

### Tool and Framework Repositories

#### 3. anthropic-quickstarts
**URL**: https://github.com/anthropics/anthropic-quickstarts
**Purpose**: Quick start templates and example applications
**Use Cases**:
- Learning API integration patterns
- Rapid prototyping
- Reference implementations
- Project templates

**Contains**:
- Customer support chatbot examples
- Computer use demos
- Tool use examples
- Streaming response patterns

---

#### 4. courses (Anthropic Courses)
**URL**: https://github.com/anthropics/courses
**Purpose**: Educational materials for prompt engineering and AI application development
**Use Cases**:
- Learning prompt engineering
- API best practices
- Advanced techniques
- Team training materials

**Topics Covered**:
- Prompt engineering fundamentals
- Tool use and function calling
- Multi-turn conversations
- Vision capabilities
- Performance optimization

---

#### 5. prompt-eng-interactive-tutorial
**URL**: https://github.com/anthropics/prompt-eng-interactive-tutorial
**Purpose**: Interactive prompt engineering tutorial
**Use Cases**:
- Training developers on Claude API
- Learning effective prompting
- Hands-on practice

---

### Developer Tools

#### 6. anthropic-tools (if available)
**URL**: https://github.com/anthropics/anthropic-tools
**Purpose**: Utility tools and helper libraries
**Use Cases**:
- API testing and debugging
- Token counting
- Response validation
- Development utilities

---

## Integration Patterns

### Pattern 1: Simple API Call

**When to Use**: Single-turn Q&A, text generation, content creation

**Reference**: anthropic-sdk-python, anthropic-sdk-typescript

**Implementation**:
```python
# Python
client = anthropic.Anthropic(api_key=os.environ.get("ANTHROPIC_API_KEY"))
message = client.messages.create(
    model="claude-opus-4-6",
    max_tokens=1024,
    messages=[{"role": "user", "content": "Explain quantum computing"}]
)
```

---

### Pattern 2: Streaming Responses

**When to Use**: Real-time chat, progressive content generation, UX optimization

**Reference**: anthropic-quickstarts (streaming examples)

**Implementation**:
```typescript
// TypeScript
const stream = await client.messages.create({
  model: 'claude-sonnet-4-5-20250929',
  max_tokens: 1024,
  messages: [{ role: 'user', content: 'Write a story' }],
  stream: true,
});

for await (const event of stream) {
  if (event.type === 'content_block_delta') {
    process.stdout.write(event.delta.text);
  }
}
```

---

### Pattern 3: Tool Use (Function Calling)

**When to Use**: AI agents, database queries, API integrations, dynamic actions

**Reference**: anthropic-quickstarts (tool use examples), courses

**Implementation**:
```python
# Python
tools = [
    {
        "name": "get_weather",
        "description": "Get current weather for a location",
        "input_schema": {
            "type": "object",
            "properties": {
                "location": {"type": "string", "description": "City name"}
            },
            "required": ["location"]
        }
    }
]

message = client.messages.create(
    model="claude-opus-4-6",
    max_tokens=1024,
    tools=tools,
    messages=[{"role": "user", "content": "What's the weather in Tokyo?"}]
)
```

---

### Pattern 4: Multi-Turn Conversation

**When to Use**: Chatbots, interactive assistants, context-aware applications

**Reference**: courses, anthropic-quickstarts (customer support examples)

**Implementation**:
```python
# Python
conversation = [
    {"role": "user", "content": "What's the capital of France?"},
    {"role": "assistant", "content": "The capital of France is Paris."},
    {"role": "user", "content": "What's its population?"}
]

message = client.messages.create(
    model="claude-sonnet-4-5-20250929",
    max_tokens=1024,
    messages=conversation
)
```

---

### Pattern 5: Vision Capabilities

**When to Use**: Image analysis, OCR, document processing, visual Q&A

**Reference**: anthropic-sdk-python, anthropic-sdk-typescript (vision examples)

**Implementation**:
```python
# Python
import base64

with open("image.jpg", "rb") as f:
    image_data = base64.b64encode(f.read()).decode("utf-8")

message = client.messages.create(
    model="claude-opus-4-6",
    max_tokens=1024,
    messages=[
        {
            "role": "user",
            "content": [
                {
                    "type": "image",
                    "source": {
                        "type": "base64",
                        "media_type": "image/jpeg",
                        "data": image_data,
                    },
                },
                {"type": "text", "text": "Describe this image"}
            ],
        }
    ],
)
```

---

### Pattern 6: Prompt Caching

**When to Use**: Repeated system prompts, large context documents, cost optimization

**Reference**: anthropic-sdk-python (caching examples)

**Implementation**:
```python
# Python
message = client.messages.create(
    model="claude-sonnet-4-5-20250929",
    max_tokens=1024,
    system=[
        {
            "type": "text",
            "text": "You are a helpful assistant...",
            "cache_control": {"type": "ephemeral"}
        }
    ],
    messages=[{"role": "user", "content": "Hello"}]
)
```

---

## Best Practices from Official Repos

### Error Handling

**Reference**: anthropic-sdk-python, anthropic-sdk-typescript

```python
# Python
from anthropic import APIError, APIConnectionError, RateLimitError

try:
    message = client.messages.create(...)
except RateLimitError:
    # Handle rate limiting (wait and retry with exponential backoff)
    pass
except APIConnectionError:
    # Handle connection errors
    pass
except APIError as e:
    # Handle other API errors
    print(f"API error: {e}")
```

---

### Token Management

**Best Practices**:
- Monitor token usage via response metadata
- Use `max_tokens` to control output length
- Implement prompt caching for large context
- Track costs per request

```python
# Python
message = client.messages.create(...)
print(f"Input tokens: {message.usage.input_tokens}")
print(f"Output tokens: {message.usage.output_tokens}")
```

---

### Security

**Best Practices**:
- Never hardcode API keys
- Use environment variables or secret managers
- Implement rate limiting
- Validate and sanitize user inputs
- Use HTTPS for all API calls

```python
# Python - Secure API key management
import os
from anthropic import Anthropic

# ✅ Good: Use environment variable
client = Anthropic(api_key=os.environ.get("ANTHROPIC_API_KEY"))

# ❌ Bad: Hardcoded key
# client = Anthropic(api_key="sk-ant-...")
```

---

## When to Reference Each Repository

| Use Case | Primary Repository | Secondary Reference |
|----------|-------------------|---------------------|
| Python backend integration | anthropic-sdk-python | anthropic-quickstarts |
| TypeScript/React frontend | anthropic-sdk-typescript | anthropic-quickstarts |
| Learning prompt engineering | courses | prompt-eng-interactive-tutorial |
| Building AI agents | anthropic-quickstarts (tool use) | courses |
| Chatbot development | anthropic-quickstarts | anthropic-sdk-* |
| Vision/OCR applications | anthropic-sdk-* (vision examples) | - |
| Cost optimization | anthropic-sdk-* (caching) | courses |
| Team training | courses | prompt-eng-interactive-tutorial |

---

## Staying Up-to-Date

### Monitor for Updates

**Watch these repositories**:
- anthropic-sdk-python (new SDK features)
- anthropic-sdk-typescript (new SDK features)
- anthropic-quickstarts (new examples and patterns)
- courses (new educational content)

### Check Release Notes
- SDK releases include new features, bug fixes, performance improvements
- API updates announced in release notes and documentation
- New model releases (e.g., Claude Opus 4.6, Sonnet 4.5)

### Community Resources
- Anthropic Developer Discord
- GitHub Issues and Discussions
- Official Anthropic documentation: https://docs.anthropic.com

---

## Common Issues and Solutions

### Issue 1: Rate Limiting

**Solution**: Implement exponential backoff, use batch API for large volumes

**Reference**: anthropic-sdk-python (error handling examples)

---

### Issue 2: Large Context Handling

**Solution**: Use prompt caching, implement context pruning

**Reference**: anthropic-sdk-python (caching examples)

---

### Issue 3: Streaming Not Working

**Solution**: Check async/await usage, verify stream handling

**Reference**: anthropic-quickstarts (streaming examples)

---

### Issue 4: Tool Use Errors

**Solution**: Validate tool schema, check required parameters

**Reference**: anthropic-quickstarts (tool use examples), courses

---

## Example: Full-Stack AI Application Reference

**Scenario**: Build a customer support chatbot with tool use

**Architecture**:
- **Frontend**: TypeScript/React (anthropic-sdk-typescript)
- **Backend**: Python/FastAPI (anthropic-sdk-python)
- **Features**: Streaming, tool use, conversation history

**Reference Path**:
1. Start with anthropic-quickstarts (customer support example)
2. Use anthropic-sdk-typescript for frontend streaming
3. Use anthropic-sdk-python for backend tool execution
4. Reference courses for advanced prompting techniques
5. Implement patterns from anthropic-quickstarts (error handling, retry logic)

---

## Quick Reference Links

| Repository | URL |
|------------|-----|
| Python SDK | https://github.com/anthropics/anthropic-sdk-python |
| TypeScript SDK | https://github.com/anthropics/anthropic-sdk-typescript |
| Quickstarts | https://github.com/anthropics/anthropic-quickstarts |
| Courses | https://github.com/anthropics/courses |
| Prompt Engineering Tutorial | https://github.com/anthropics/prompt-eng-interactive-tutorial |
| Official Docs | https://docs.anthropic.com |
| API Reference | https://docs.anthropic.com/en/api |

---

## Usage Instructions for Team

**For Software Engineers**:
- Always check official SDKs first for implementation patterns
- Use quickstarts for rapid prototyping and examples
- Reference courses for prompt engineering best practices

**For Tech Director**:
- Review architecture patterns in quickstarts for technical decisions
- Stay updated on SDK releases for new capabilities
- Ensure team follows best practices from official examples

**For QA Expert**:
- Test against patterns in official examples
- Verify error handling matches SDK recommendations
- Validate token usage and performance

---

**Version**: 1.0
**Last Updated**: 2026-02-11
**Maintained By**: Tech Director, Software Engineer
