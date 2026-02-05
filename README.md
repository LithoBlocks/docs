# LithoBlocks Documentation

This repository contains the documentation for [LithoBlocks](https://app.lithoblocks.com), a platform for building and sending Slack message templates with dynamic data, interactive buttons, and webhooks.

## About LithoBlocks

LithoBlocks lets you create reusable Slack message templates, fill them with dynamic data, and send them to your workspace. Connect Slack once, then design templates with placeholders, blocks, and interactive buttons. The platform supports integrations with low-code platforms (Make, Zapier, n8n, Airtable, Retool) and AI agent frameworks (LangChain, LlamaIndex, CrewAI).

## Documentation structure

This documentation site is built with [Mintlify](https://mintlify.com) and includes:

- **Getting started guides**: Quickstart, connecting Slack, and onboarding
- **Template guides**: Placeholders, blocks, directives, versioning, and sample data
- **Interactive features**: Buttons, button webhooks, message updates, and modals
- **Advanced topics**: Entities, webhook destinations, and architecture
- **Integration guides**: Low-code platforms and AI agent frameworks
- **API reference**: Complete API documentation generated from OpenAPI spec

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally:

```bash
npm i -g mint
```

Run the development server at the root of this repository (where `docs.json` is located):

```bash
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Changes are automatically deployed to production when pushed to the default branch. The GitHub app is configured to propagate changes from this repository to the Mintlify deployment.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on:
- File layout and organization
- Content types and structure (Diátaxis framework)
- MDX components and best practices
- Writing conventions

## Troubleshooting

- **Dev environment won't start**: Run `mint update` to ensure you have the most recent version of the CLI
- **Page loads as 404**: Make sure you're running `mint dev` in the folder containing `docs.json`
- **Navigation issues**: Verify page paths in `docs.json` match file locations (without `.mdx` extension)

## Resources

- [Mintlify documentation](https://mintlify.com/docs)
- [LithoBlocks Dashboard](https://app.lithoblocks.com)
- [Support](mailto:support@lithoblocks.com)
