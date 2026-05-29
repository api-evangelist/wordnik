# Wordnik (wordnik)

Wordnik is the largest online English dictionary by number of words. Its v4 REST API exposes definitions from five dictionaries, etymologies, real example sentences from millions of sources, audio pronunciations, related-word relationships, frequency over time, hyphenation, bi-gram phrases, scrabble scores, random words, reverse-dictionary lookup, word-of-the-day, and authenticated user word lists.

**URL:** [Visit APIs.json URL](https://developer.wordnik.com)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Dictionaries, Dictionary, Word Data, English, Lexicography, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### Wordnik

The v4 Wordnik API exposes single-word lookups (definitions, etymologies, examples, pronunciations, related words, frequency, hyphenation, phrases, scrabble score, audio), cross-word discovery (random word, search, reverse dictionary, word of the day), and authenticated user word-list management. Authentication is a single api_key query parameter; user-scoped operations require an auth_token header obtained via /account.json/authenticate.

**Human URL:** [https://developer.wordnik.com](https://developer.wordnik.com)

**Base URL:** `https://api.wordnik.com/v4`

#### Tags:

 - Dictionary, Word Data, Lexicography, English

#### Properties

- [Documentation](https://developer.wordnik.com/docs)
- [GettingStarted](https://developer.wordnik.com/gettingstarted)
- [OpenAPI](openapi/wordnik-openapi.yml)
- [Python SDK](https://pypi.org/project/wordnik-py3/)
- [Python 2 SDK (legacy)](https://pypi.org/project/wordnik/)
- [Ruby SDK](https://rubygems.org/gems/wordnik)
- [PHP SDK](https://github.com/wordnik/wordnik-php)
- [Java SDK](https://github.com/wordnik/wordnik-clients/tree/master/java)
- [Kotlin SDK](https://github.com/wordnik/wordnik-clients/tree/master/kotlin)
- [Scala SDK](https://github.com/wordnik/wordnik-clients/tree/master/scala)
- [Android SDK](https://github.com/wordnik/wordnik-clients/tree/master/android-java)
- [Objective-C SDK](https://github.com/wordnik/wordnik-clients/tree/master/objc)
- [Naftiko Capability — Word](capabilities/wordnik-word.yaml)
- [Naftiko Capability — Words](capabilities/wordnik-words.yaml)
- [Naftiko Capability — Word List](capabilities/wordnik-word-list.yaml)
- [Naftiko Capability — Word Lists](capabilities/wordnik-word-lists.yaml)
- [Naftiko Capability — Account](capabilities/wordnik-account.yaml)

## Common Properties

- [Website](https://wordnik.com)
- [Documentation](https://developer.wordnik.com)
- [Pricing](https://developer.wordnik.com/pricing)
- [GettingStarted](https://developer.wordnik.com/gettingstarted)
- [Signup](https://www.wordnik.com/signup)
- [Blog](https://blog.wordnik.com)
- [StatusPage](https://github.com/wordnik/wordnik-status)
- [GitHubOrganization](https://github.com/wordnik)
- [Support](mailto:apiteam@wordnik.com)
- [TermsOfService](https://www.wordnik.com/about)
- [Plans](plans/wordnik-plans-pricing.yml)
- [RateLimits](rate-limits/wordnik-rate-limits.yml)
- [FinOps](finops/wordnik-finops.yml)
- [Vocabulary](vocabulary/wordnik-vocabulary.yml)
- [SpectralRuleset](rules/wordnik-rules.yml)
- [JSONLDContext](json-ld/wordnik-context.jsonld)
- [Open Source — Wordnik Public Word List](https://github.com/wordnik/wordlist)
- [Open Source — NYT First Said](https://github.com/wordnik/nyt-first-said)
- [Open Source — Language Museums Dataset](https://github.com/wordnik/language-museums)
- [PublicAPIsListing](https://github.com/public-apis/public-apis)

## Features

| Name | Description |
|------|-------------|
| Five Dictionary Sources | Definitions are drawn from American Heritage (ahd-5), Wiktionary, Webster, Century, and WordNet — selectable per request via sourceDictionaries. |
| Real-World Example Sentences | Examples come from millions of sources rather than constructed example text, with citation metadata via /word.json/{word}/examples and /topExample. |
| Audio Pronunciations | AHD mp3 audio pronunciations exposed via /word.json/{word}/audio with time-expiring fileUrls. |
| Word Graph Relationships | Synonym, antonym, hypernym, hyponym, rhyme, and 17 other relationship types via /word.json/{word}/relatedWords. |
| Frequency Over Time | Annual usage counts from 1800 onward via /word.json/{word}/frequency for historical / linguistic research. |
| Reverse Dictionary | Natural-language query to candidate words via /words.json/reverseDictionary. |
| Word Of The Day | Curated daily word with definitions, examples, and editorial notes via /words.json/wordOfTheDay. |
| User Word Lists | Authenticated users can create, edit, and curate named word lists via /wordList.json and /wordLists.json. |

## Use Cases

| Name | Description |
|------|-------------|
| Dictionary App | Build a consumer-facing dictionary or thesaurus app using definitions, etymologies, pronunciations, and examples. |
| Word Games | Power crossword, scrabble, hangman, and word-discovery games using random words, search, and scrabble scoring. |
| Vocabulary Learning | Build a flashcard or vocabulary-coach app using user word lists, word of the day, and definitions across grade levels. |
| Editorial Tooling | Surface synonyms, antonyms, and reverse-dictionary lookup inside CMS / writing tools. |
| Linguistic Research | Use frequency-over-time data and the word-graph for academic linguistics and lexicographic research. |
| Children's Education | Use the forthcoming children's / student definitions tier for age-appropriate vocabulary apps. |

## Integrations

| Name | Description |
|------|-------------|
| Python (wordnik-py3) | Official Python 3 client published to PyPI as `wordnik-py3`. |
| Ruby (wordnik) | Official Ruby gem published to RubyGems as `wordnik`. |
| PHP | Swagger-generated PHP client in wordnik/wordnik-php. |
| Java | Swagger-generated Java client in wordnik/wordnik-clients/java. |
| Kotlin / Scala / Android / Objective-C | Additional swagger-generated clients in wordnik/wordnik-clients. |

## Solutions

| Name | Description |
|------|-------------|
| Dictionary-Of-Record Integration | Use Wordnik as the canonical dictionary for a product surface, hitting /word.json/{word}/definitions with sourceDictionaries selection logic. |
| Quota-Aware Caching Layer | Cache results aggressively per-word and use /account.json/apiTokenStatus telemetry plus X-RateLimit headers to right-size the Hobby / Pro / Enterprise tier. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Wordnik v4 API](openapi/wordnik-openapi.yml) — OpenAPI 3.0.3, 24 paths, 28 operations, 37 schemas, two security schemes (api_key query, auth_token header), 5 tags (Word, Words, Word List, Word Lists, Account).

### JSON Schema

37 standalone JSON Schema (Draft 2020-12) files in [`json-schema/`](json-schema/), one per OpenAPI component schema, including `WordObject`, `Definition`, `Example`, `WordOfTheDay`, `WordList`, `AuthenticationToken`, `ApiTokenStatus`, and 30 others.

### JSON Structure

37 corresponding [JSON Structure](https://json-structure.org) files in [`json-structure/`](json-structure/), converting JSON Schema types and formats into the strict-typed JSON Structure type system (`int32`, `int64`, `double`, `datetime`, `date`, `uri`, etc.).

### JSON-LD

- [`json-ld/wordnik-context.jsonld`](json-ld/wordnik-context.jsonld) — Single JSON-LD 1.1 context document declaring 37 type terms and 116 property terms in the `wordnik:` namespace, with schema.org alignments for `name`, `description`, `url`, `email`, `dateCreated`, `dateModified`, and `datePublished`.

### Examples

37 example JSON payload files in [`examples/`](examples/), one per JSON Schema, generated deterministically from the property-name heuristics.

## Capabilities

Naftiko capabilities organized as self-contained per-tag definitions. Each file inlines its own `consumes` block plus REST and MCP exposers — no shared or imported references. (Naftiko 1.0.0-alpha2.)

| Capability | Operations | Tag |
|------------|-----------|-----|
| [Wordnik — Word](capabilities/wordnik-word.yaml) | 11 | Word |
| [Wordnik — Words](capabilities/wordnik-words.yaml) | 5 | Words |
| [Wordnik — Word List](capabilities/wordnik-word-list.yaml) | 6 | Word List |
| [Wordnik — Word Lists](capabilities/wordnik-word-lists.yaml) | 1 | Word Lists |
| [Wordnik — Account](capabilities/wordnik-account.yaml) | 5 | Account |

## Plans & Pricing

- [`plans/wordnik-plans-pricing.yml`](plans/wordnik-plans-pricing.yml) — API Commons Plans 0.1. Four tiers: **Basic** ($0, 100 req/hr, free for nonprofit/research), **Hobby** ($10/mo, 1,000 req/hr), **Pro** ($59/mo, 20,000 req/hr), **Enterprise** ($149/mo, 45,000 req/hr).

## Rate Limits

- [`rate-limits/wordnik-rate-limits.yml`](rate-limits/wordnik-rate-limits.yml) — API Commons Rate Limits 0.1. Per-key hourly ceilings (100 / 1,000 / 20,000 / 45,000 req/hr) plus a per-minute burst ceiling. Telemetry via `x-ratelimit-remaining-hour`, `x-ratelimit-remaining-minute`, `x-ratelimit-limit-hour`, `x-ratelimit-limit-minute` response headers. Throttled responses use HTTP 429.

## FinOps

- [`finops/wordnik-finops.yml`](finops/wordnik-finops.yml) — FinOps Framework 1.0, FOCUS-aligned (data spec v1.3). Pricing category: Tiered Subscription. Three meters: `api_requests` (request), `subscription_month` (month), `hourly_quota_window` (hour). Visibility via `/account.json/apiTokenStatus` + `x-ratelimit-*` response headers.

## Vocabulary

- [`vocabulary/wordnik-vocabulary.yml`](vocabulary/wordnik-vocabulary.yml) — Unified taxonomy mapping 5 resources, 7 actions, 5 workflows, and 8 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [`rules/wordnik-rules.yml`](rules/wordnik-rules.yml) — 37 Spectral rules across 13 categories enforcing Wordnik API conventions (lowerCamel.json paths, camelCase parameters, PascalCase schema names, Title Case operation summaries, api_key/auth_token security schemes).

## Type

- **x-type:** company
- **x-tier:** 2 (enriched from public-apis bulk registration with full OpenAPI + capability pipeline)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Dictionaries

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
