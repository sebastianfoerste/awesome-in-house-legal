# Awesome In-House Legal [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of open-source projects that do real work for in-house legal teams: contracts, e-signature, legal AI, legal operations, investigations, compliance, and the datasets used to evaluate legal AI tools.

Curated by [IN-HOUSE APAC](https://inhouseapac.com), the membership community for in-house legal counsel across Asia-Pacific. Every entry was verified against its live repository before inclusion. Star counts and activity notes are as of June 2026.

**A note on licenses.** Several projects here use AGPL, BSL, or fair-code licenses. Those are fine for self-hosted internal use in most cases, but review the license before embedding any of them in a product or service. You are the legal team; this is the one diligence step you cannot skip.

## Contents

- [Document Automation and Assembly](#document-automation-and-assembly)
- [E-Signature](#e-signature)
- [Contract Review and Redlining](#contract-review-and-redlining)
- [Legal AI and NLP](#legal-ai-and-nlp)
- [Legal Operations and Knowledge](#legal-operations-and-knowledge)
- [Investigations and E-Discovery](#investigations-and-e-discovery)
- [Compliance, Privacy and Governance](#compliance-privacy-and-governance)
- [Legal Datasets and Benchmarks](#legal-datasets-and-benchmarks)
- [Contributing](#contributing)

## Document Automation and Assembly

- [docassemble](https://github.com/jhpyle/docassemble) - Guided-interview and document assembly engine built by a lawyer-programmer; turns repeat documents (NDAs, policies, intake forms) into self-service questionnaires that output finished DOCX/PDF. The closest thing to an open-source standard in legal document automation. `Python` `MIT` `~950★`
- [docassemble-AssemblyLine](https://github.com/SuffolkLITLab/docassemble-AssemblyLine) - Suffolk LIT Lab's framework and question library for converting paper legal forms into runnable guided web apps on docassemble, much faster than building interviews from scratch. `Python` `MIT` `~60★`
- [docxtemplater](https://github.com/open-xml-templating/docxtemplater) - Generates Word, PowerPoint, and Excel files from templates with placeholders, loops, and conditions. Legal owns the Word template; systems fill in parties, dates, and clauses. `JavaScript` `MIT/GPL dual` `~3.6k★`
- [Wraft](https://github.com/wraft/wraft) - Document lifecycle platform for authoring and distributing structured business documents (letters, contracts) with version control and PDF output via Typst/LaTeX. `Elixir` `AGPL-3.0` `~145★`
- [Accord Project Template Archive](https://github.com/accordproject/template-archive) - Smart legal contract templating (formerly Cicero) that binds natural-language clause text to data models, making terms like payment schedules and SLAs machine-readable and executable. `TypeScript` `Apache-2.0` `~350★`

## E-Signature

- [DocuSeal](https://github.com/docusealco/docuseal) - Self-hostable DocuSign alternative with drag-and-drop templates, multi-signer routing, and API automation. No per-envelope fees, and signed documents stay on your infrastructure. `Ruby` `AGPL-3.0` `~17.1k★`
- [Documenso](https://github.com/documenso/documenso) - Polished open-source signing platform built on Next.js and PostgreSQL, with audit trails. The most active community in the category. `TypeScript` `AGPL-3.0` `~13.3k★`
- [OpenSign](https://github.com/OpenSignLabs/OpenSign) - Lightweight self-hosted signing for routine NDAs, engagement letters, and approvals, with digital-certificate support, timestamping, and webhooks. Runs on minimal hardware. `JavaScript` `AGPL-3.0` `~6.5k★`
- [LibreSign](https://github.com/LibreSign/libresign) - Digital signing inside Nextcloud, with workflows, roles, and audit logs. Useful where the company already runs Nextcloud for files. `PHP` `AGPL-3.0` `~770★`

## Contract Review and Redlining

- [OpenContracts](https://github.com/Open-Source-Legal/OpenContracts) - Self-hosted document intelligence platform with human annotation, structured extraction, citation graphs, vector search, and a built-in MCP server, so AI answers about your contracts come with citations instead of black-box chat. `Python/TypeScript` `MIT` `~1.4k★`
- [LegalQuants lq-ai](https://github.com/LegalQuants/lq-ai) - Self-hosted legal AI workbench for playbook-driven first-pass contract review (seeded NDA, MSA, and DPA playbooks), runs against your choice of model including air-gapped local inference. Young project; evaluate maturity before production use. `Python` `Apache-2.0` `~65★`
- [Ally Legal Assistant](https://github.com/Azure-Samples/ally-legal-assistant) - Microsoft reference architecture for an AI contract reviewer inside Word itself: summarisation, in-document Q&A, policy compliance checks, and auto-markup on your own Azure tenant. A blueprint, and a product is left as an exercise. `JavaScript/Python` `~75★`
- [redlines](https://github.com/houfu/redlines) - Python library that compares two texts and outputs Word-style track-changes redlines in Markdown, HTML, or terminal formats. Built by a Singapore-based legal engineer; drops a comparison step into any review pipeline. `Python` `MIT` `~160★`
- [legal-redline-tools](https://github.com/evolsb/legal-redline-tools) - Turns structured contract-review output into deliverables lawyers actually send: tracked-changes .docx with accept/reject markup, redline PDFs, and tier-grouped negotiation memos with fallback positions. `Python` `MIT` `~34★`

## Legal AI and NLP

- [Presidio](https://github.com/microsoft/presidio) - Microsoft's PII detection and de-identification framework for text, images, and structured data. The standard answer to "redact the personal data before it goes to the LLM", relevant under PDPA, PIPL, and APPI alike. `Python` `MIT` `~8.6k★`
- [LexNLP](https://github.com/LexPredict/lexpredict-lexnlp) - Information extraction from unstructured legal text: dates, money, durations, citations, conditions, clause classification. A building block for processing large contract sets without a vendor platform. Maintenance has slowed; AGPL needs review before embedding. `Python` `AGPL-3.0` `~780★`
- [ContraxSuite](https://github.com/LexPredict/lexpredict-contraxsuite) - Full open-source contract analytics platform (ingestion, OCR, ML clause extraction, review UI) built on LexNLP. Dormant since 2022 but remains the seminal reference for what self-hosted contract analytics looks like. `Mixed` `AGPL-3.0` `~180★`
- [Blackstone](https://github.com/ICLRandD/Blackstone) - spaCy pipeline and model for NLP over unstructured legal text (case names, citations, instruments, provisions, courts), trained on English-law material. Research-grade and largely dormant, still a good learning resource. `Python` `Apache-2.0` `~690★`
- [eyecite](https://github.com/freelawproject/eyecite) - High-performance legal citation extraction and resolution from the Free Law Project; powers CourtListener. US-citation focused. `Python` `BSD-2-Clause` `~250★`
- [LawGlance](https://github.com/lawglance/lawglance) - RAG-based legal assistant built with LangChain and ChromaDB, currently trained on Indian statutes. A working reference implementation a team can fork and re-point at its own jurisdiction or internal policies. `Python` `Apache-2.0` `~270★`
- [ChatLaw](https://github.com/PKU-YuanGroup/ChatLaw) - Open legal LLM family fine-tuned for Chinese law, with released weights, from Peking University. The leading open model for Greater China matters. `Python` `AGPL-3.0` `~7.5k★`
- [OpenNyAI](https://github.com/OpenNyAI/Opennyai) - NLP pipeline for Indian legal documents: named entity recognition, extractive summarisation, and rhetorical role labelling of judgments. India is a major APAC jurisdiction underserved by US/UK tooling. `Python` `MIT` `~95★`
- [LexGLUE](https://github.com/coastalcph/lex-glue) - Benchmark code and datasets for legal language understanding in English, from the group behind the Legal-BERT models. Useful before fine-tuning your own legal models. `Python` `~260★`

## Legal Operations and Knowledge

- [n8n](https://github.com/n8n-io/n8n) - Workflow automation with 400+ integrations and native AI capabilities. The legal-ops glue for intake routing, contract-approval handoffs, and matter-status notifications; self-hosting keeps privileged data inside the firewall. `TypeScript` `Fair-code` `~192k★`
- [Outline](https://github.com/outline/outline) - Fast, collaborative team knowledge base with granular permissions. A clean home for legal playbooks, fallback positions, and self-serve FAQs the business can search instead of emailing legal. `TypeScript` `BSL-1.1` `~39k★`
- [BookStack](https://github.com/BookStackApp/BookStack) - Self-hosted wiki organised into books, chapters, and pages. The structure maps naturally to a policy library: one book per contract type or jurisdiction playbook, with role-based access for sensitive guidance. `PHP` `MIT` `~18.8k★`
- [Formbricks](https://github.com/formbricks/formbricks) - Open-source survey and form platform. Replaces ad-hoc email with structured legal intake (contract requests, incident reports) that pipes straight into a triage workflow while data stays on your server. `TypeScript` `AGPL-3.0` `~12.4k★`
- [Captable](https://github.com/captableinc/captable) - Open-source cap table and securities management positioned as a Carta alternative, with a built-in data room. Development appears stalled since mid-2025; evaluate maintenance risk first. `TypeScript` `AGPL-3.0` `~810★`

## Investigations and E-Discovery

- [Aleph](https://github.com/alephdata/aleph) - Searches and browses large collections of documents and structured data, surfacing the people and companies inside them. Built for investigative journalism; equally suited to internal investigations and due diligence. Active development has moved to OpenAleph. `Python/JavaScript` `MIT` `~2.4k★`
- [OpenAleph](https://github.com/openaleph/openaleph) - The actively maintained successor fork of Aleph, from the Data and Research Center. The go-forward choice for self-hosted investigation and document-search workloads. `Python/JavaScript` `MIT` `~95★`
- [Datashare](https://github.com/ICIJ/datashare) - Self-hosted document search from the ICIJ with OCR, named-entity extraction, and batch search. Battle-tested at Panama and Pandora Papers scale; useful for investigations, subject access requests, and discovery scoping. `Java` `AGPL-3.0` `~740★`
- [FreeEed](https://github.com/shmsoft/FreeEed) - Open-source e-discovery processing engine (Tika, Lucene, Solr) with OCR and review support. A no-license-fee way to process and cull custodian data before deciding what goes to outside counsel or a paid platform. `Java` `Apache-2.0` `~140★`
- [CourtListener](https://github.com/freelawproject/courtlistener) - Searchable archive of US court opinions, oral arguments, judges, and federal filings, with free docket alerts. Most useful to APAC teams with US litigation exposure. `Python` `AGPL` `~950★`

## Compliance, Privacy and Governance

- [CISO Assistant](https://github.com/intuitem/ciso-assistant-community) - GRC platform covering risk assessment, audit, and compliance management with built-in support for 150+ frameworks (ISO 27001, SOC 2, NIS2, DORA, GDPR, PCI DSS). A free, self-hostable system of record for compliance posture. `Python` `AGPL-3.0` `~4.1k★`
- [Comply](https://github.com/strongdm/comply) - SOC 2 compliance automation that generates policy documents from Markdown templates and tracks audit obligations as tickets in Jira/GitHub/GitLab. Dormant since 2021, but the templates remain widely used. `Go` `Apache-2.0` `~1.6k★`
- [Fides](https://github.com/ethyca/fides) - Privacy engineering platform for data mapping, consent management, and automated fulfilment of data subject access and deletion requests. Automates the operational core of privacy compliance that legal owns. `Python/TypeScript` `Apache-2.0` `~460★`
- [Open Terms Archive](https://github.com/OpenTermsArchive/engine) - Tracks the terms of service and privacy policies of online services and keeps a versioned archive of every change. Evidence-grade monitoring of vendor terms instead of discovering unilateral amendments after the fact. `JavaScript` `EUPL-1.2` `~130★`
- [Open Policy Agent](https://github.com/open-policy-agent/opa) - CNCF-graduated policy engine that enforces rules written as declarative code. The reference implementation of policy-as-code: legal-approved rules on data residency, access, or retention get encoded once and enforced automatically by engineering. `Go` `Apache-2.0` `~11.8k★`
- [Klaro](https://github.com/klaro-org/klaro-js) - Lightweight self-hosted consent management for third-party scripts and cookies, with GDPR/ePrivacy-style consent flows. `JavaScript` `BSD-3-Clause` `~1.5k★`
- [CookieConsent](https://github.com/orestbida/cookieconsent) - Dependency-free, GDPR-compliant cookie consent banner with granular per-category consent. The fastest route to a defensible banner across corporate sites and microsites. `JavaScript` `MIT` `~5.5k★`
- [Giskard](https://github.com/Giskard-AI/giskard) - Evaluation and testing library for LLM agents, including a vulnerability scanner for hallucination, bias, and security issues. Gives AI-governance owners a repeatable way to test vendor and internal AI systems against the failure modes their policies require them to manage. `Python` `Apache-2.0` `~5.4k★`

## Legal Datasets and Benchmarks

How do you know whether a legal AI tool is any good? You test it against these.

- [CUAD](https://github.com/TheAtticusProject/cuad) - The Contract Understanding Atticus Dataset: 500+ commercial contracts expert-annotated across 41 clause categories. The standard benchmark for whether a contract-review AI can actually find the assignment, change-of-control, and indemnity clauses you care about. `Dataset, CC BY 4.0`
- [LegalBench](https://github.com/HazyResearch/legalbench) - Open-science benchmark of 160+ legal reasoning tasks contributed by 40+ lawyers and academics. The most load-bearing public yardstick for "is this LLM actually good at legal reasoning?" `Benchmark`
- [Pile of Law](https://github.com/Breakend/PileOfLaw) - A ~256GB corpus of legal and administrative text for pretraining and evaluating legal language models. Also a reference point for asking vendors what their models were trained on. `Dataset`
- [LawBench](https://github.com/open-compass/LawBench) - 20 tasks across memorisation, understanding, and application for evaluating LLMs on Chinese law, with published results for 51 models. GPT-4 topped out at 52 percent zero-shot, a useful calibration on how far legal AI still has to go. `Benchmark, Apache-2.0`
- [LBox Open](https://github.com/lbox-kr/lbox-open) - Multi-task benchmark and 150k-precedent corpus for Korean legal language understanding and judgment prediction. The principal open dataset for evaluating legal AI on Korean law. `Dataset, CC BY-NC 4.0`

## Contributing

Suggestions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) for the curation standards, then open an issue or pull request.

## About

Maintained by [IN-HOUSE APAC](https://inhouseapac.com), the membership community for in-house legal counsel across Asia-Pacific. For commercial legal AI tools, see our [Legal AI Directory](https://inhouseapac.com).

Licensed under [CC0 1.0](LICENSE).
