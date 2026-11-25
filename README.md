# RupeeRise: Fact-Checking an AI-Written Investor Brief

**A FinTech case study on catching AI hallucinations before they reach investors.**

**Repository:** `rupeerise-ai-fact-check-log`  
**Topics:** `generative-ai` · `ai-hallucination` · `fact-checking` · `prompt-engineering` · `fintech` · `responsible-ai` · `case-study`  
**Author:** Ankush Verma · BBA (FinTech), Chitkara Business School · **Tools:** Gemini, ChatGPT, Perplexity · November 2026

---

## The case
**RupeeRise** (fictional) is a digital lending app in Bengaluru. Its founder asked AI to write an investor brief on India's digital lending and UPI market and wanted to send it as-is. Acting as a Business Analyst, I audited every factual claim, citation, and regulatory reference against official primary sources before the document could reach investors.

## What I did
| Step | Task | Tool |
|---|---|---|
| 1 | Generated the same investor brief prompt across two AI models | Gemini, ChatGPT |
| 2 | Scored both drafts on 5 evaluation criteria | Manual |
| 3 | Extracted 10 core claims and prompted the AI to self-rate its confidence | AI + Manual |
| 4 | Verified every claim against primary regulatory sources (RBI, NPCI, PIB) | Official websites |
| 5 | Audited every link and inline citation returned by an AI search engine | Perplexity |

## Results
| Metric | Result |
|---|---|
| Claims checked | 10 |
| Correct | 2 |
| Outdated / Distorted / Fabricated / Unsupported | 4 / 1 / 1 / 2 |
| Rated "High confidence" by AI but wrong | 4 |
| Perplexity citations that fully supported the claim | 2 of 3 inline citations (24 total links listed) |
| Tool comparison score (Gemini vs ChatGPT, /10) | 7 vs 9 |

## Worst error I found
* **The AI's Claim:** The brief cited a fabricated Reserve Bank of India (RBI) circular number (`RBI/2023-24/112`) claiming that digital lending apps are permitted to hold customer funds in internal escrow accounts for up to 7 business days before settlement, alongside an invented executive quote.
* **What the Official Source Says:** Under the actual **RBI Guidelines on Digital Lending (September 2, 2022)**, all loan disbursals and repayments must execute directly between the bank accounts of the borrower and the Regulated Entity (RE)—Lending Service Providers (LSPs) like RupeeRise are strictly prohibited from holding funds in any pass-through or pool account.
* **Why It Would Mislead an Investor:** Presenting a non-existent regulatory exemption makes RupeeRise's proposed fund-flow architecture appear compliant when it is actually illegal, exposing the startup to immediate regulatory shutdown and destroying investor trust during due diligence.

## My top 3 "What not to do" rules
1. **Never publish AI-generated regulatory circular numbers, exact market figures, or executive quotes without checking primary sources** (evidence: C3, C5).
2. **Never use an AI's self-reported "High Confidence" score as a proxy for factual accuracy** (evidence: C1, C4, C5, C8).
3. **Never assume a footnote or URL proves a claim—always open the link to verify it points to an official report rather than an unrelated page or raw API endpoint** (evidence: C9, C10).

## My answer to the founder
**Do not send this brief to investors.** 80% of the factual claims in the draft are outdated, distorted, unsupported, or completely fabricated—including false regulatory claims that would fail basic legal due diligence. Before sharing, we must replace every AI-generated statistic and regulatory reference with verified figures pulled directly from NPCI monthly product statistics, RBI master directions, and PIB releases.

## Skills shown
AI Output Evaluation · Fact-Checking with Official Sources · Hallucination Detection · Citation & Link Auditing · Responsible AI in Finance · Indian FinTech & Regulatory Knowledge

## What I learned
- AI writes confident, fluent, investor-ready prose even when underlying facts are outdated or completely fabricated.
- Exact transaction volumes, regulatory circular numbers, executive quotes, and source names are the highest-risk failure points for LLMs.
- An AI's own confidence rating is not proof; only an official primary source (RBI, NPCI, PIB, or audited company filings) counts as verification.
- A cited link is not proof either—links must be opened and verified to confirm they actually support the exact claim and aren't dead links or raw API endpoints.
- Different AI models produce noticeably different accuracy and structural quality on the same prompt, making head-to-head benchmarking essential.
- Nothing AI-written should ever reach investors, regulators, or customers without a structured human-in-the-loop audit.

---

*Disclaimer: RupeeRise and the investor brief audited in this repository are fictional scenarios created for academic and portfolio learning.*
