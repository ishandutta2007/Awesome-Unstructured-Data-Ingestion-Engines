# Awesome-Unstructured-Data-Ingestion-Engines

## Top Unstructured Data Ingestion Engines Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Document Parsing, Layout Extraction & LLM-Ready Data Transformation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Unstructured Data Ingestion Engines**. These tools transform complex, legacy PDFs, scans, spreadsheets, and web content into structured JSON, Markdown, and chunked outputs — ready for RAG pipelines, AI agents, and downstream data workflows.

**Examples** include Unstructured.io, LlamaParse, Firecrawl, Reducto, Landing AI, Docsumo, Sensible, Azure AI Document Intelligence, AWS Textract, and Google Document AI (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom parsing pipelines, and transparent document processing — ideal for teams prioritizing data sovereignty, developers building ingestion pipelines, and organizations avoiding per-page API costs.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Unstructured.io](https://unstructured.io/)**  
  Leading document ingestion platform with API for partitioning, enrichment, chunking, and embedding files into AI-ready data. Features production-grade vision transformer models, fine-tuned OCR, by-page and by-similarity chunking, and compliance (SOC 2 Type 2, HIPAA, GDPR, ISO 27001, FedRAMP). Business plans include SaaS, dedicated VPC, and in-VPC deployment. Free tier for prototyping; paid plans scale by page volume [citation:1][citation:14].

- **[LlamaParse](https://www.llamaindex.ai/)**  
  GenAI-native document parser from LlamaIndex designed for RAG and agent workflows. Supports PDF, PPTX, DOCX, XLSX, HTML with table recognition, multimodal parsing (images/diagrams), and custom parsing prompts. V2 introduces tier-based pricing: Fast (1 credit/page), Cost Effective (3 credits/page), Agentic (10 credits/page), Agentic Plus (45 credits/page). Version pinning for production stability. Free tier: 1,000 pages/day [citation:2][citation:15].

- **[Firecrawl](https://www.firecrawl.dev/)**  
  Web scraping and ingestion API for AI applications. Converts websites into clean Markdown, structured JSON, or LLM-ready chunks. Features scrape, crawl, map, search, and agent endpoints with Cloudflare bypass. Free tier: 500-1,000 pages/month. Paid plans from Hobby ($11/month for 3,000 pages) to Scale ($764/month for 1M pages) [citation:3][citation:16].

- **[Reducto](https://reducto.ai/)**  
  Agentic document platform for complex PDFs and scans. Parse API delivers layout-aware OCR, table extraction with merged cells, handwriting recognition, and bounding-box citations. Independently verified #1 in LongExtractBench with 99.6% precision/recall across 225 documents averaging 358 pages. Powers production workflows at Harvey, Scale AI, and Vanta. Deployment options: cloud, VPC, on-prem, air-gapped [citation:4][citation:17].

- **[Landing AI](https://landing.ai/)**  
  Agentic Document Extraction (ADE) Gen2 with complexity-based pricing as low as $0.01/page. Parse and Extract APIs with hierarchical block structure, stable IDs, Markdown span pointers, and standardized outputs (HTML tables, checkbox states). Two service tiers: Standard (0.5x price) and Priority. Designed for high-volume, repeatable extraction with schema-driven fields and semantic matching [citation:5][citation:18].

- **[Docsumo](https://docsumo.com/)**  
  Intelligent document processing with MCP server for AI agent integration. Agents Builder automates multi-step workflows: ingestion → classification → extraction → validation → export. Document types with configurable fields, cases, tables, and workflow orchestration. Human-in-the-loop approvals. Rate limit: 10 req/sec per account [citation:6][citation:19].

- **[Sensible](https://sensible.so/)**  
  Developer-first document data extraction with SenseML query language combining LLM techniques and layout-based rules. Supports PDFs, emails, spreadsheets, images. Features preprocessors, conditional extraction, validations, confidence scores, and human review UI. DevOps platform with metrics dashboard and production monitoring [citation:7][citation:20].

- **[Azure AI Document Intelligence](https://azure.microsoft.com/en-us/products/ai-services/ai-document-intelligence)**  
  Cloud-based document analysis with prebuilt and custom models for structured data extraction from forms, invoices, receipts, and IDs.

- **[AWS Textract](https://aws.amazon.com/textract/)**  
  Managed ML service for extracting text, handwriting, tables, and forms from documents without ML experience.

- **[Google Document AI](https://cloud.google.com/document-ai)**  
  Document understanding platform with pre-trained processors for invoices, receipts, forms, and OCR.

## Open-Source GitHub Projects

- **[Docxtract](https://github.com/mohammadmaso/Docxtract)**  
  Self-hosted web application extracting structured data from unstructured documents using LLMs. Visual schema builder with drag-and-drop field editor (nested objects, arrays, all JSON Schema types). Multi-LLM support (OpenAI, Anthropic, Google). AI schema suggestion, semantic chunking for large documents (>50K chars), batch processing, background jobs via Celery, and JSON/CSV export. Django + React + Pydantic AI stack. Dockerized with PostgreSQL [citation:11].

- **[harvest-agent](https://pypi.org/project/harvest-agent/)**  
  Open-source AI web scraper with Cloudflare bypass and LLM extraction. Features four scraping modes (full, economy, hybrid, auto) balancing content preservation vs token efficiency. `llm-extract` command uses local LLM (Ollama, OmniRoute, any OpenAI-compatible API) to return structured JSON from natural language prompts. Zero external API costs [citation:8].

- **[pdfmux](https://pypi.org/project/pdfmux/)**  
  PDF extraction with **Certify Anything** verification layer. Audits any extraction engine's output (Reducto, LlamaParse, Docling, Mistral OCR, in-house parsers) against source PDF and identifies **silently dropped pages** — the failure mode that poisons RAG indexes without errors. Batch verification across directories with PASS/REVIEW/FAIL verdicts, confidence scores, and coverage metrics. MIT licensed [citation:10].

- **[universal-doc-parser](https://pypi.org/project/universal-doc-parser/)**  
  Streaming document parser with bounded memory consumption (<250 MB RSS regardless of document length). Features auto-tuner (coordinate-descent optimizer for template-specific configs), observability system with metrics collector, HTML telemetry dashboard, and FastMCP server for Claude Desktop integration. Benchmarks against Docling, Surya/Marker, and Unstructured.io using TEDS, CER/WER metrics [citation:9].

- **[hirara-web](https://pypi.org/project/hirara-web/)**  
  Self-hosted web search and fetch service for AI agents. Features SSRF perimeter guard, robots.txt honoring, `/context/urls` trust boundary for URL authorization, and untrusted content delimiters. SearXNG engine selection with measured benchmarks across 12 engines. Cache-aware design for agent loops. Docker Compose deployment with loopback binding [citation:12].

- **[Docling](https://github.com/DS4SD/docling)**  
  Open-source document parsing library with lightweight local-friendly extraction for digital-born PDFs. Produces clean Markdown output optimized for LLM workflows. Best for clean, text-layer documents rather than degraded scans.

- **[PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)**  
  Open-source OCR toolkit with PaddleOCR-VL vision-language model for document understanding. ONNX export, multiple quantization options (fp32, q8, quint8, q4), and API provider fallbacks (Gemini, OpenAI) when local GPU unavailable.

- **[DocTR](https://github.com/mindee/doctr)**  
  Open-source OCR library from Mindee supporting PyTorch and TensorFlow. Structured output with JSON containing blocks, lines, words, and bounding boxes. Table detection with dense grid output, reading order linearization, and Markdown/HTML export.

### Additional Strong Open-Source Options

- **[Unstructured Open Source](https://github.com/Unstructured-IO/unstructured)** — Core library powering the Unstructured API with partitioning, enrichment, and chunking. Apache 2.0 licensed .
- **[Apache Tika](https://github.com/apache/tika)** — Content detection and extraction toolkit supporting 1,000+ file formats. Apache 2.0 licensed.
- **[PyMuPDF](https://github.com/pymupdf/PyMuPDF)** — High-performance PDF parsing with text, image, and table extraction. AGPL licensed.
- **Vector Databases** — Qdrant, Weaviate, Milvus for embedding storage and semantic retrieval.
- **Workflow Orchestration** — Apache Airflow, Prefect, Temporal for scheduling ingestion pipelines.

**Frameworks for building custom systems**: Combine **Docxtract** for LLM-powered schema extraction, **harvest-agent** for web content ingestion with LLM structuring, **pdfmux** for silent-drop certification, **universal-doc-parser** for memory-bounded parsing, and **hirara-web** for agent-safe web fetching to build a complete self-hosted unstructured data ingestion stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Unstructured data ingestion engines must comply with data protection regulations (GDPR, CCPA), industry standards (SOC 2, HIPAA), and document retention policies.
- Self-hosted open-source solutions require proper security hardening, GPU infrastructure planning, and model monitoring.

---

**Made for data engineers, AI developers, RAG pipeline builders, and developers transforming complex documents into structured data.**  
Let's make unstructured data ingestion more open, accurate, and data-sovereign.
