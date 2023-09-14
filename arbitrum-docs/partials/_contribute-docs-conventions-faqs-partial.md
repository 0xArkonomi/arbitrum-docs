---

### Document type conventions

Every document should be a specific _type_ of document. Each type of document has its own purpose:

| Document type       | Purpose                                                                            | Example(s) to refer to                                                                                                                                          |
| ------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gentle introduction | Onboard a specific reader audience with tailored questions and answers             | [A gentle introduction to Orbit](../launch-orbit-chain/orbit-gentle-introduction.md)                                                                            |
| Quickstart          | Onboard a specific reader audience with step-by-step "learn by doing" instructions | [Quickstart: Build dApps](/for-devs/quickstart-solidity-hardhat.md)                                                                                             |
| How-to              | Provide task-oriented procedural guidance                                          | [How to run a local dev node](../node-running/how-tos/local-dev-node.mdx)                                                                                       |
| Concept             | Explain what things are and how they work                                          | [Token bridging](../for-devs/concepts/token-bridge/token-bridge-erc20.mdx) <br/>[Nodes and networks](https://docs.prylabs.network/docs/concepts/nodes-networks) |
| FAQ                 | Address frequently asked questions                                                 | [FAQ: Run a node](../node-running/faq.md)                                                                                                                       |
| Troubleshooting     | List common troubleshooting scenarios and solutions                                | [Troubleshooting: Run a node](../node-running/troubleshooting-running-nodes.md)                                                                                 |
| Reference           | Lists and tables of things, such as API endpoints and developer resources          | [RPC endpoints and providers](../node-running/node-providers.mdx)                                                                                               |

This isn't an exhaustive list, but it includes most of the document types that we use.

### Style conventions

The following style guidelines provide a number of loose recommendations that help us deliver **a consistent content experience** across our docs:

1.  **Casing**
    - Sentence-case "content labels": document titles, sidebar titles, menu items, section headers, etc.
2.  **Linking**
    - Avoid anchoring links to words like "here" or "this". Descriptive anchor text can help set expectations for readers who may hesitate to click on ambiguous links.
3.  **Separate procedural from conceptual (most of the time)**
    - Within procedural docs like how-tos and quickstarts, avoid including too much conceptual content. Provide only the conceptual information that the target reader _needs_ in order to complete the task at hand. Otherwise, organize conceptual information within conceptual docs, and link to them "just in case" from other docs.
4.  **Voice**
    - Address the reader as "you".
    - Write like you'd speak to a really smart friend who's in a rush.
    - Opt for short, clear sentences that use translation-friendly, plain language.
    - Use contractions wherever it feels natural - this can help convey a friendly and conversational tone.
5.  **Formality**
    - Don't worry too much about formality. The most valuable writing is writing that provides value to readers, and readers generally want to "flow" through guidance.
    - Aim at "informal professionalism" that prioritizes **audience-tailored problem-solving** and **consistent style and structure**.
6.  **Targeting**
    - Don't try to write for everyone; write for a _specific reader persona_ (also referred to as "audience" in this document) who has a _specific need_.
    - Make assumptions about prior knowledge (or lack thereof) and make these assumptions explicit in the beginning of your document.
7.  **Flow**
    - **Set expectations**: Begin documents by setting expectations. Who is the document for? What value will it provide to your target audience? What assumptions are you making about their prior knowledge? Are there any prerequisites?
    - **Value up front**: Lead with what matters most to the reader persona you're targeting. Then, progressively build a bridge that carries them towards task completion as efficiently as possible.
8.  **Cross-linking**
    - We want to maintain both **high discoverability** and **high relevance**. As a general rule of thumb, links to other docs should be "very likely to be useful for most readers". Every link is a subtle call to action; we want to avoid CTA overload.
9.  **Things to avoid**
    - **Symbols where words will do**: Minimize usage of `&` and `/` - spell out words like "_and_" and "_or_".
    - **Jargon**: Using precise technical terminology is ok, as long as your target audience is likely to understand the terminology. When in doubt, opt for clear, unambiguous, _accessible_ language.

Don't stress too much about checking off all of these boxes; we periodically review and edit our most heavily-trafficked docs, bringing them up to spec with the latest style guidelines.

Some important disclaimers:

- **This isn't an exhaustive list**. These are just the min-bar guidelines that will be applied to all new content moving forward.
- **Many of our docs don't yet follow this guidance**. Our small-but-mighty team is working on it! If you notice an obvious content bug, feel free to submit an [issue](https://github.com/OffchainLabs/arbitrum-docs/issues) or [PR](https://github.com/OffchainLabs/arbitrum-docs/pulls).

### Banner conventions

You can use banners (Docusaurus refers to them as ["admonitions"](https://docusaurus.io/docs/markdown-features/admonitions)) to set expectations for your readers and to emphasize important callouts. Use these conservatively, as they interrupt the flow of the document.

#### Public preview content banner

Example:

<PublicPreviewBannerPartial />

Usage:

```
import PublicPreviewBannerPartial from '../partials/_public-preview-banner-partial.md';

<PublicPreviewBannerPartial />
```

<br />

#### Under construction banner

Example:

:::caution UNDER CONSTRUCTION

The following steps are under construction and will be updated with more detailed guidance soon. Stay tuned, and don't hesitate to click the `Request an update` at the top of this document if you have any feedback along the way.

:::

Usage:

```
:::caution UNDER CONSTRUCTION

The following steps are under construction and will be updated with more detailed guidance soon. Stay tuned, and don't hesitate to click the `Request an update` at the top of this document if you have any feedback along the way.

:::
```

<br />

#### Community member contribution banner

Example:

:::info Community member contribution

The following document was contributed by @todo-twitter-handle. Give them a shoutout if you find it useful!

:::

Usage:

```
:::info Community member contribution

The following document was contributed by @todo-twitter-handle. Give them a shoutout if you find it useful!

:::
```

### Organization conventions

Our published docs are generally organized like this in the sidebar:

```
📄 Gentle introduction
📄 Quickstart
📂 How-tos
  📄 Write a smart contract
📂 Concepts
  📄 Smart contract
📁 Reference
📄 Troubleshooting
📄 FAQ
📄 Glossary
📄 Contribute docs
📂 Third-party content
  📁 Product A
  📂 Product B
    📄 How to test your smart contract using Product B
```

- This isn't a strict requirement; it's a loose guideline.
- Not all product areas have all types of content.
- Deviating from this pattern can make important content more discoverable to readers. For example, [Developer tools and resources](https://developer.arbitrum.io/for-devs/dev-tools-and-resources/overview) is a root-level collection of reference-type content.
- The sidebar structure that you see in our published docs is determined by the [`sidebars.js` file](https://github.com/OffchainLabs/arbitrum-docs/blob/master/website/sidebars.js) located at the root of the `website` directory.
  - You may notice that our sidebars are currently organized using plain-old objects that specify individual files and folders.
  - We're moving away from this "manual configuration" and towards convention-based [auto-generated sidebars](https://docusaurus.io/docs/sidebar/autogenerated).
  - To ensure that this new approach works with your docs, **all net-new content should be organized within a folder structure that matches the desired sidebar structure**.

<br />

---

### Frequently asked questions

#### Can I point to my product from core docs? For example - if my product hosts a public RPC endpoint, can I add it to your [RPC endpoints and providers](/node-running/node-providers) page?

These types of contributions are generally **not merged** unless they're submitted by employees of Offchain Labs.

Instead of opening a PR for this type of contribution, click the `Request an update` button at the top of the published document to create an issue. Generally, third-party services are included in core docs only if we can confidently assert that the services are "**trustworthy, highly relevant to the core document at hand, and battle-tested by Arbitrum developers**" under a reasonable amount of scrutiny.

#### Can I use AI-generated content?

"No". By issuing PRs into our docs repo, you're acknowledging that your content has been produced organically. Content produced under the influence of AI/ML tooling, such as ChatGPT, is "strictly not allowed".

#### Should I be wary of contributing to FAQs and Glossaries? It looks like there are some automations configured against these document types.

You're right! We draft FAQs and Glossaries on Notion to make it easier for nontechnical internal contributors to contribute. This content is then published to our docs repo using a script that reads from Notion and writes to Markdown.

You can still submit changes to the Glossary and FAQ markdown files; we manually synchronize these types of changes with Notion content whenever we need to.

#### How long does it take for my third-party content contribution to be reviewed?

Our small-but-mighty team is continuously balancing competing priorities, so we can't guarantee a specific turnaround time for third-party docs PRs. They're processed in the order in which they're received, generally within a week or two.

#### Is there any way to expedite third-party content contribution reviews?

The most effective way to expedite processing is to ensure that your PR incorporates the conventions outlined in this document. Please don't ask for status updates - if you've submitted a PR, it's on our radar!
