# Milo — Shopping That Understands Older Adults

**DubHacks '26 · Team project · Portfolio case study**

A voice-based shopping prototype designed to help older adults purchase everyday essentials with greater independence, while incorporating safeguards against suspicious requests and unintended purchases.

[Project submission](https://devpost.com/software/milo-shopping-that-understands-older-adults) · [Demo video](https://www.youtube.com/watch?v=4YVUp6x_Y4Q) · [Original team repository](https://github.com/svedison/Dubhacks-26-Team-Meditation)

## My role — Risk and Transactions

I was responsible for the risk and transaction module and contributed to product design, testing, and the final presentation.

- **Risk and transaction logic:** Implemented trusted-catalog checks, risky-product blocking, alternative-product responses, simulated payments, and order recording.
- **Visa sandbox integration:** Contributed to sandbox account validation and its integration with the transaction flow. Purchases remained simulated; this was not a live payment integration.
- **Product experience and privacy:** Contributed a personal story about my grandmother and me to inform the product direction, and participated in decisions about guardian permissions and how older adults share purchase records. This was personal experience informing design, rather than formal user research.
- **Testing and interface validation:** Used AI assistance to develop and run tests covering risk checks, orders, sharing filters, and duplicate requests.
- **Presentation:** Prepared product messaging, slides, speaking notes, the demo video script, and judge Q&A materials.

The project outcomes below describe the team's work. My individual contributions are limited to the responsibilities listed above.

## The problem

Conventional online shopping can create barriers for people who find small screens, complex checkout flows, and product searches difficult to use. Milo explores how conversational purchasing can reduce those barriers while preserving the shopper's control.

## The experience

The prototype uses an iPad as a talking picture frame, paired with a family-facing mobile interface. A shopper can request a familiar item using a nickname, hear purchase details, and confirm by voice. Product context and purchase history help resolve requests without requiring exact brand names.

## Risk and trust considerations

The team's design combines conversational interaction with checks before purchase:

| Risk | Prototype approach |
| --- | --- |
| Untrusted products | Restrict purchasing to a curated product catalog and offer alternatives for unsupported requests. |
| Scam pressure | Identify suspicious language, interrupt the purchase flow, and alert family. |
| Unintended quantities | Question unusually large requests and apply quantity controls. |
| Payment information exposure | Validate the stored account through Visa's sandbox and retain a sanitized validation outcome in the order. |
| Excessive family visibility | Filter the family interface according to the shopper's privacy setting. |
| External service failure | Provide fallback interaction and local safety behavior. |

These are prototype design choices, not evidence of production fraud-detection accuracy, regulatory compliance, or real-world safety effectiveness. Sandbox account validation is distinct from a live payment authorization or settlement.

## Team-reported prototype results

The Devpost submission describes a four-scene demonstration on an iPad and phone, a catalog of 100 products, and 101 backend tests alongside frontend and module tests. It also describes voice reordering, reminders, stock tracking, and sandbox account validation.

These results are attributed to the team submission; this case study does not independently verify the implementation or test results. Live payment integration and a senior-center pilot are described as future work.

## Technology

The submission lists React, Vite, TypeScript, Fastify, SQLite, WebSocket, Silero VAD, Deepgram, Claude, MiniMax TTS, and Visa sandbox integration.

## Collaboration and attribution

Milo was created by a four-person team. Devpost credits Jiayi Zhu, Ziwei Yu, jiuxin77, and 奕晨 卢. The original repository is maintained under the `svedison` GitHub account.

This repository is a personal case study of a team project. It does not contain a copy of the team's implementation or claim sole authorship. The personal contribution section reflects my responsibilities; the broader product and technical results are credited to the team.

## Reflection

Milo illustrates a product tradeoff: reducing shopping friction while retaining meaningful checks before a transaction. A next evaluation would measure task completion, incorrect item selection, false scam alerts, and user understanding of confirmations and privacy settings.

## Sources

- [Milo project submission on Devpost](https://devpost.com/software/milo-shopping-that-understands-older-adults)
- [Team repository and planning documents](https://github.com/svedison/Dubhacks-26-Team-Meditation)

Project details are based on the public submission reviewed on October 27, 2026; individual responsibilities are supplied by the case-study author. Proposed evaluation measures above are case-study reflections, not completed project results.
