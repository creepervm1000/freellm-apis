# Contributing

[中文版](CONTRIBUTING_zh.md)

Thanks for wanting to contribute. This list is meant to be actually useful, so there are some strict rules about what gets added.

## Adding a Provider

Before submitting a PR to add a new provider, make sure it meets **all** of these requirements:

1. **Actually free.** No credit card required, no trial that auto-charges, no "free but you need to add a payment method first." If a user has to put in payment info to access the free tier, it does not belong here.

2. **Provides API access.** Web UIs, chatbots, and "try it in your browser" pages do not count. The provider must offer programmatic access via an API (REST, WebSocket, or similar). CLI tools count if they can be scripted.

3. **Currently working.** Test it yourself before submitting. Make an actual API call. If the provider is down, returning errors, or the free tier is no longer available, don't submit it.

4. **Useful models.** The free models should be capable of handling real tasks. A 0.5B parameter model that can barely form sentences does not count. The model should be able to write code, answer questions, or perform useful tasks at a reasonable quality level.

5. **No fake providers.** Do not submit providers that you haven't personally tested. Do not submit providers that require you to sign up through a referral link to get access. Do not submit providers hosted on sketchy domains with no documentation.

## What Will Get Your PR Rejected

- **Fake or unverified providers.** If you can't demonstrate that it works, it won't be added.
- **Dead links.** If the sign-up page, API docs, or endpoint is down, it won't be added.
- **Providers that require payment info for free access.** This is a dealbreaker. No exceptions.
- **Providers that only offer chat UIs.** No API = no entry.
- **Providers with unusable free models.** If the free tier only offers a model that can't complete a basic coding task, it's not useful enough for this list.
- **Providers hosted on obviously temporary infrastructure.** If the domain is `free-llm-api-2024.herokuapp.com`, it's not going to last.
- **Copy-paste submissions.** If your provider description is copied from the provider's marketing page without any actual testing or personal experience, it will be removed.

## PR Format

When adding a provider, follow this format:

```markdown
### Provider Name

| Detail | Info |
|--------|------|
| **Models** | Model names |
| **API Endpoint** | The API base URL |
| **Sign Up** | [Link to sign up](https://example.com) |
| **Auth** | How authentication works |
| **Rate Limits** | Known rate limits |
| **Credit Card** | Required / Not required |
| **Notes** | Any important details |

Description of the provider, how to use it, and why it's useful. Be specific about the free tier limitations. Include any tips for getting the most out of it.
```

Also add a row to the Quick Comparison table in both the English and Chinese READMEs.

## Removing a Provider

If a provider's free tier is no longer available, open an issue or PR with evidence (screenshot, error log, or updated terms page). The provider will be removed or marked as inactive.

## Translations

All documentation files (README, CONTRIBUTING, CODE_OF_CONDUCT) must have Chinese translations. When updating the English version, update the Chinese version too. Add cross-links between language versions.

## Questions?

Open an issue before submitting a PR if you're unsure whether a provider qualifies.