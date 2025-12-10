Buzzwords
- disparate data sources
- data types
- thickness of data (stories versus ngrams)
- big data; swamped by massive datasets. 
- raw data
- maintaining datasets
- data pipelines
- structured data
- (robust) data platform
- data-driven research
- survey data; people provide annotated datasets.
- open data

### Fleeting Notes

*instructions*
  - describe planned user interactions and a community-driven approach
  - Provide a timeline including a proof-of-concept demonstration of the key components
  - Describe software or data cyberinfrastructure services and how they follow industry best practices, including the architecture of the CI and the engineering process to be used for the design, development, documentation, testing, validation, and release of the software and its deployment to the end-user community. The description of the CI architecture and processes should explain how security/privacy, trustworthiness, provenance, transparency, reproducibility, and usability will be addressed by the project and integrated into the proposed system and the engineering process, and how adaptability to new technologies and changing requirements will be addressed by the project and built into the proposed system, as appropriate
  - Include an acceptance and evaluation plan that involves end users
  - Discuss how the infrastructure will support the integrity and provenance of the scientific workflow and resulting data artifacts, in the context of balancing the security and usability of the infrastructure in a way that directly supports the underlying science drivers and objectives
  - Describe how the proposed CI will be secured and protected against attack, and against being used as an attack vector 
  - Describe how the CI will facilitate secure sharing of data or software artifacts, including descriptions of what approaches will be utilized to aid users

![[Storywrangler-ecosystems.pdf]]

## 2025-11-17: Section 3.1 ctd: phase 3 and 4 and 3.2

### Section 3.1.
#### Phase 3: Engagement

Phase 3 expands Storywrangler's user base through active community outreach while maintaining curatorial standards that prioritize quality over quantity. Rather than passively accepting submissions, we combine editorial curation with proactive engagement in the computational social science community to build awareness and trust.

Core team members actively participate in relevant communities where our target users already congregate. Kendall Fortney's engagement with the CURIOSS (Consortium for Understanding and Sustaining the Research Software Workforce) provides direct access to research software engineers and computational social scientists. The team's involvement with PyData Vermont demonstrates ongoing commitment to open-source community building and provides a local venue for workshops and feedback sessions. The Vermont Complex Systems Institute hosts the International Conference on Computational Social Science (IC2S2) in 2026, providing an unparalleled opportunity to demonstrate an early prototype Storywrangler to computational social scientists during the platform's early growth phase. We leverage these networks through: (1) presenting Storywrangler at IC2S2 2026 and other domain conferences, (2) hosting bi-annual workshops at venues like PyData Vermont and through CURIOSS, (3) conducting training sessions on pipeline integration and entity resolution, and (4) participating in open-source community events (e.g., csv,conf, PyData). These activities build awareness among researchers who would benefit from Storywrangler while demonstrating our commitment to the broader open science ecosystem.

Researchers submit proposals through a simple web form providing their repository URL and justification for integration. Our editorial board will meet bi-weekly and review submissions, selecting ≥5-10 pipelines per year based on scientific value, code quality, entity standard adherence, and licensing compatibility. This selective approach, combined with our active outreach, ensures we integrate high-quality contributions that showcase what's possible rather than accepting everything submitted. The VCSI's reputation signals to the community that Storywrangler-integrated datasets meet rigorous reproducibility standards.

Accepted pipelines receive DOIs via UVM Dataverse for both dataset outputs and the pipeline itself, enabling researchers to cite their data contributions as scholarly products. Unlike depositing code on GitHub alone, Storywrangler integration provides: (1) persistent identifiers for citation in publications, (2) discoverability through our platform and cross-dataset queries enabled by shared entity identifiers, (3) VCSI endorsement signaling code quality and reproducibility, and (4) ongoing usability as infrastructure rather than abandoned supplementary materials. Workshops and training sessions explicitly demonstrate these benefits to potential contributors.

We implement bi-annual structured evaluation with users recruited through our workshops and outreach activities. Each cycle includes: (1) usability testing with researchers attempting to query APIs and explore datasets, (2) feedback sessions with pipeline submitters on the integration process, (3) surveys assessing platform value and pain points, and (4) documentation review identifying gaps. This feedback directly informs ongoing development and standards refinement, ensuring Storywrangler evolves in response to community needs rather than our assumptions.

During Phase 3, we retain ownership of standards governance while actively soliciting community input through the Storywrangler Standards Repository. Workshop participants and pipeline submitters can propose new entity types, suggest schema modifications, or report ambiguities. Our editorial meetings review these proposals, iteratively refining standards based on real integration challenges and community feedback.

The adapter framework enables researchers to integrate existing projects with minimal refactoring—a key message in our training sessions. Submitters either conform outputs to our standard schema or include adapter code using our templates and validation tools (pdp-helper). Workshops provide hands-on experience with this process, lowering barriers to entry.

#### Phase 4: Sustainability

Phase 4 establishes Storywrangler as permanent institutional infrastructure under VCSI stewardship. Givent the institution commitment to quality control and reproducibility standards, we Storywrangler maintain editorial curation. Phase 4 formalizes governance structures, secures long-term funding, and ensures technical maintenance continues beyond the grant period. The goal is transitioning from grant-funded project to institutionally-supported service with community input mechanisms but retained editorial authority.

Governance of the Storywrangler platform will be formalized through a steering committee representing multiple labs and stakeholders. This committee will include Dodds, Danforth, Woodward, Fortney, Arnold, Lovato, Zhang, and St-Onge, meeting biannually to review pipeline submissions, approve standards updates, and set strategic priorities. While community members can propose entity standards, request features, and report issues through the Storywrangler Standards Repository, final decisions rest with the steering committee to maintain scientific rigor and institutional accountability. All decisions will follow a transparent, documented process with meeting agendas and notes published in the Storywrangler Organization repository. Governance adheres to open-source best practices: transparent decision-making, clear contribution guidelines, standardized licensing across repositories, published code of conduct, and community feedback loops via GitHub Discussions.

Long-term operation requires institutional commitment beyond grant funding. VCSI will formally adopt Storywrangler as core infrastructure, providing ongoing hosting, storage, and personnel support. We will pursue NSF sustainment funding to support continued development and scale infrastructure as adoption grows. Storage and compute costs will be monitored throughout Phases 1-3 to inform realistic post-grant budgets. Personnel continuity is ensured through VCSI's commitment to maintaining dedicated technical staff rather than relying solely on graduate students or postdocs whose tenure is temporary.

Continuous integration and deployment (CI/CD) pipelines will automate testing, security scanning, and dependency updates across the platform. As entity identifier systems evolve (e.g., Wikidata grows, ORCID policies change), our standards must adapt accordingly. We will implement schema versioning with backward compatibility, migration guides for existing pipelines, and automated validation tools (pdp-helper) that check compliance against current standards. Adapter code templates will be maintained as reference implementations, updated as best practices evolve. All platform releases will be archived in UVM Dataverse with DOIs, ensuring long-term reproducibility even as the platform evolves.

The Storywrangler API will remain the primary access method, with comprehensive documentation maintained using OpenAPI standards. For researchers preferring programmatic access, we will develop client libraries for Python and R that handle authentication, pagination, and error handling. The Storywrangler Toolbox will continue evolving via packaging, workshops, or teaching of complex systems theory. Training materials, workshops, and documentation will be updated based on user feedback gathered through bi-annual evaluations and community discussions. Through these efforts, Storywrangler will establish sustainable infrastructure that supports reproducible science while maintaining the curatorial standards that distinguish it from unmoderated data repositories.


### Section 3.2.

The project activities will build on significant capabilities resulting from institutional and NSF investments, including an NSF EPSCoR RII Track I grant, "Harnessing the Data Revolution: the Science of Online Corpora, Knowledge and Stories" (SOCKS), which enabled the initial development of these computational research tools and provided a testbed for interdisciplinary expansion of users at a statewide and multi-institutional level, positioning us to scale to a national resource. As part of that grant, NSF also provided cyberinfrastructure equipment funding that allows the project team to leverage capabilities on our HPC, the Vermont Advanced Computing Center (VACC). The equipment investment of \$1M includes 2 GPU compute nodes, each with four NVIDIA H100 SXM 80GB GPUs, 64 CPU cores per node, 1TB of memory, 1 compute node with 192 CPU cores, 1.5TB memory, 600TB of high-performance storage, and 1PB of spinning disk for secondary datacenter to provide data backups to primary storage.

NSF has made other significant investments in cyberinfrastructure at UVM that positions us to support this project on a national scale, including: NSF MRI (DataMountain, a massive database cluster), NSF MRI (IceCore, a new AI supercomputer GPU cluster). DataMountain is a large memory, sharded MongoDB to support near real-time access to enormous data files, supporting projects that require such speed to analyze, describe, and explain rapidly growing datasets effectively. IceCore is UVM's newest investment in high-performance computing offering the latest NVIDIA GPU cluster. It will revolutionize our research capabilities with its state-of-the-art GPU technology giving unparalleled performance in AI and massively parallel processing. We have completed phase one of the purchase and build and it includes 16 nodes, each with: 4 NVIDIA H200 NVL 141GB HBM3e GPUs with 4-way NVLink Bridge for GPU interconnect, 192 Intel CPU cores, 1TB memory, 400Gb InfiniBand NDR for low latency interconnect between nodes, and 100Gb Ethernet networking. Phase two is currently in the active RFP state but will be a \$1.7M investment.

These infrastructure investments directly enable Storywrangler's technical architecture. The VACC GPUs support containerized pipeline execution with Podman, DataMountain's sharded MongoDB informed our approach to handling large temporal datasets (migrating proven patterns to PostgreSQL with time-series optimization), and IceCore's compute capacity ensures we can scale as community adoption grows. The investment in computational resources de-risks our ambitious Phase 1-3 timeline—we are not building infrastructure from scratch, but integrating existing capabilities into a coherent platform.

Prior NSF investment through SOCKS enabled development of api.complexstories.uvm.edu, an operational prototype serving Wikimedia page view analytics via PostgreSQL-backed API. This system currently powers wikimedia.uvm.edu and complexstories.uvm.edu, demonstrating our architectural approach at scale (50M+ data points serving real-time queries). Phase 1 builds directly on this foundation—migrating proven PostgreSQL schemas and API patterns to FastAPI while adding Pydantic validation, standardized entity identifiers, and multi-dataset support. We are not proposing speculative architecture; we are scaling what already works. Detailed metrics on this prior work are provided in Section 6: Results from Prior NSF Support.

We are also uniquely positioned to support the wide-scale adoption and use of open source tools because of other investments in our open source data and software capacity through UVM's open source program office (OSPO), VERSO, one of the leading university OSPOs in the United States. VERSO emerged from a \$1M investment from Google to build capacity in open source ecosystems and networks (the OCEAN project), which was then expanded into a formal university OSPO with \$1.2M in support from the Alfred P. Sloan Foundation. VERSO has enabled the development of open source community at a national level, including participating in the United Nations' OSPOs for Good panel and leading a national gathering of OSPOs through NSF's CURIOSS program. Having a well-established leadership role in the open source space will provide critical social and academic infrastructure for collaborating institutions and national scale participation in our computational tools, building an open source community for maintenance and adoption. VERSO's leadership also informed our decision to leverage existing open-source ecosystems (OpenAPI, Wikidata, ORCID, ROR, Podman) rather than creating proprietary standards—ensuring Storywrangler integrates with the broader research software landscape rather than operating in isolation. Further, VERSO has catalyzed the creation of the UVM Dataverse, a framework for open data sharing that is discussed in detail in our cyberinfrastructure plan. The UVM Dataverse will be greatly expanded by this project and will provide an open source repository for Storywrangler users.

Beyond infrastructure, our technical approach builds on established methodological frameworks. Team member Sam Zhang developed the PDP Helper package during his tenure as a US Research Software Sustainability Institute (URSSI) Early-Career Fellow—a fellowship program sponsored by NSF and the Alfred P. Sloan Foundation to advance research software sustainability. His ongoing collaboration with the Human Rights Data Analysis Group provides direct expertise in principled data pipeline (PDP) design, ensuring our standards align with practices proven in high-stakes human rights investigations where reproducibility and auditability are paramount.

Rather than inventing new identifier systems, we leverage international standards: Wikidata Q-codes for entities (people, concepts, institutions), ORCID for researchers, and ROR for institutions—battle-tested systems with millions of existing identifiers and active communities maintaining them. Our API documentation uses OpenAPI specifications, our validation uses Pydantic schemas, and our containerization uses Podman—all widely-adopted open source tools with extensive documentation and support communities. This choice reduces technical risk, accelerates development, and ensures Storywrangler's outputs interoperate with the broader research software ecosystem.

By building on these existing NSF investments and recognized capabilities, Storywrangler represents an evolution rather than revolution—consolidating proven prototypes, leveraging substantial infrastructure, and adopting established standards. This approach maximizes the return on prior NSF investment while minimizing technical risk, positioning the project to deliver on its ambitious timeline and scale to national adoption.

## section 3.2: Close Collaborations Among Stakeholders

\subsection{Close Collaborations Among Stakeholders}

Storywrangler's development represents a transition from statewide testbed to national infrastructure, building on established collaborations while expanding to new networks of users and contributors. The instruments are currently used by researchers spanning disciplines including linguistics, anthropology, geography, computer science, psychology, classics, mathematics, philosophy, and community development and applied economics. These users are primarily supported through a statewide ecosystem curated by Vermont EPSCoR. NSF's RII Track I (SOCKS) investment created a testbed for interdisciplinary use among an ecosystem of statewide participants including St. Michael's College, Champlain College, and Middlebury College, with modest engagement nationally and internationally with researchers at the Santa Fe Institute in New Mexico and the Complexity Science Hub in Vienna, Austria. These collaborators have provided valuable information about opportunities and challenges related to user experience across disciplines and technical barriers for entry. In our 2025 NSF reverse site visit for SOCKS, a panelist asked how we planned to expand the use of these instruments to national scale. Our response is this Storywrangler framework. This project significantly widens the aperture and enables collaboration beyond Vermont, building national networks of research participation including private sector and non-profit partners (Gallup, Wikimedia Foundation, MITRE, Google), as well as academic partners in computational social science and social, behavioral and economic complex systems research across the United States.

The project team brings together cyberinfrastructure experts, research software engineers, and domain scientists working in concert throughout development. Team member Sam Zhang developed the PDP Helper package as a URSSI Early-Career Fellow and collaborates with the Human Rights Data Analysis Group, providing expertise in principled data pipeline design. Kendall Fortney's engagement with CURIOSS (Consortium for Understanding and Sustaining the Research Software Workforce) connects the project to the research software engineering community. The team's involvement with PyData Vermont demonstrates ongoing commitment to open-source community building. These collaborations ensure Storywrangler development is informed by both research software best practices and practical community needs.

Phase 2 partners include researchers working on Science of Science projects, course catalog analysis, Women in Mathematics biographical datasets, and Wikimedia analytics. They serve as both users and contributors to infrastructure design. These partners provide diverse use cases. Some work with proprietary data requiring access controls (Legacy.com obituaries), while others work with fully open data (Wikimedia). Some need entity-level granularity (biographical data), while others need aggregate statistics (trend analysis). Partners participate actively through monthly virtual office hours, Slack discussions, and GitHub issues, providing feedback that directly shapes infrastructure refinement. This bi-directional collaboration ensures Storywrangler serves real research needs rather than speculative use cases.

The project leverages multiple networks to build national awareness and gather diverse feedback. The Vermont Complex Systems Institute hosts the International Conference on Computational Social Science (IC2S2) in Burlington in summer 2026, providing an opportunity to demonstrate Storywrangler to approximately 700 computational social scientists and conduct tutorials on the platform. Beyond IC2S2, we engage through PyData Vermont (local workshops), CURIOSS consortium (research software engineering community), domain-specific conferences (Complex Systems Society, digital humanities meetings), and open-source community events. These overlapping networks ensure we reach computational social scientists, research software engineers, digital humanists, and data journalists.

Project management follows a collaborative model balancing institutional oversight with community input. During Phases 1-2, an editorial board meeting bi-weekly reviews pipeline submissions and partner feedback. This board includes project PIs and technical leads, ensuring decisions reflect both strategic vision and implementation realities. In Phase 3, this formalizes into a steering committee meeting biannually to review community submissions, approve standards updates, and set strategic priorities. While community members can propose standards and request features through the Storywrangler Standards Repository (GitHub), final decisions rest with the steering committee to maintain scientific rigor. VCSI's reputation depends on quality curation. All decisions follow a transparent process with meeting agendas and notes published in the Storywrangler Organization repository. Detailed management structure is provided in the supplementary three-page document on management and coordination.

Multiple engagement channels accommodate varying researcher preferences: monthly virtual office hours for informal discussion, Slack for quick questions, GitHub for tracked issues and feature requests, bi-annual structured evaluations (Phase 3), and workshops providing hands-on training. Through these collaborations, Storywrangler develops as a genuinely collaborative effort. CI experts inform technical choices, domain scientists shape infrastructure through use, national networks provide feedback, and transparent governance ensures accountability. This collaborative approach maintains the curatorial standards that distinguish Storywrangler from unmoderated repositories.
## 2025-11-16: Section 3.1 ctd

### **Phase 1: Consolidation & Infrastructure work**

Phase 1 establishes the Storywrangler platform infrastructure foundation by applying PDP standards to our own existing tools, demonstrating by example what we'll later require from community submissions. This phase builds on significant existing work: our team includes a core member Sam Zhang collaborating with the Human Rights Data Analysis Group, and we have operational prototypes including api.complexstories.uvm.edu which already serve the Wikimedia interface with endpoints that will migrate to Storywrangler. During Year 1, we pursue five interconnected steps in parallel, with repository refactoring and standards development informing each other through iterative cycles. 

**(1) Repository consolidation and standards development:** 
Establish a dedicated Storywrangler GitHub organization housing our refactored datasets and tools with consistent MIT licensing, citation-ready READMEs, and comprehensive documentation. Simultaneously, create the Storywrangler Standards Repository (similar to OpenAPI-Specification) defining accepted entity identifier systems (Wikidata Q-codes, ORCID, ROR) and validation requirements. **Our collaboration with HRDAG provides direct expertise in PDP design,** ensuring our standards align with established best practices. As we refactor each tool, we document entity matching patterns and adapter requirements, with each refactored pipeline serving as a reference implementation.

(2) Containerization procedures:
Develop standardized Podman containerization for each refactored pipeline, with Dockerfiles generated from existing dependency specifications (requirements.txt, environment.yml). **Containerization provides both reproducibility and security:** containers run in isolated sandboxes with strict resource limits (CPU, memory, execution time) and **restricted network access limited to our API endpoint only**. Containers can POST results to Storywrangler but cannot access arbitrary internet resources. Podman's rootless architecture prevents privilege escalation, while ephemeral containers—destroyed immediately after execution—eliminate persistent attack vectors. This security model, validated with our own pipelines in Phase 1, will protect our infrastructure when accepting community contributions in Phase 3.

**Adapter Layer:** 
Adapter code runs **inside containerized pipelines**, serving as the integration point between pipeline outputs and our backend API. Researchers include adapter code in their repositories that validates entity IDs against standards from (1), transforms outputs to API schemas via Pydantic validation, and POSTs to our backend endpoints. **The container's restricted networking—limited to our API endpoint—ensures pipelines cannot exfiltrate data or access external resources.** These initial adapters—written for our own refactored tools in Phase 1—establish reference implementations and template patterns that community contributors will adapt in Phase 3. By having submitters write their own adapters, we avoid becoming a bottleneck while maintaining security through network isolation.

**(3) Backend application development:** 
Implement PostgreSQL database with time-series optimized schemas and FastAPI application. We migrate proven patterns from our operational prototype (api.complexstories.uvm.edu), which currently serves Wikimedia page view data via PostgreSQL-backed endpoints. Central to this is defining Pydantic schemas that formalize the entity standards from (1)—these schemas serve dual purposes: adapters use them to validate pipeline outputs before submission, and the backend API uses them to validate incoming data. This shared schema definition ensures consistency between pipeline integration (adapters) and data serving (API). All endpoints will be documented using OpenAPI specifications, which are auto-generated from our Pydantic models.

(4) Data publication: 
Publish our initial refactored datasets in UVM Dataverse with DOIs, ensuring each dataset is linked to its generating pipeline and includes comprehensive metadata, entity matching provenance, and confidence scores. **Our Phase 1 datasets include both fully open and proprietary sources** (e.g., Wikimedia page views, Legacy.com obituaries under data use agreement). **We reconcile this through a dual-access model:** highly aggregated, non-identifying outputs are published openly in Dataverse (e.g., temporal n-gram frequencies, divergence metrics), while our tiered API provides access-controlled queries to more granular data for authenticated researchers. Raw proprietary data remains secured within containerized execution environments and is never exposed. This approach enables open science principles (FAIR, citable outputs) while respecting copyright, privacy, and licensing constraints.

(5) Interface integration: 
Demonstrate API integration with existing external interfaces (wikimedia.uvm.edu, complexstories.uvm.edu) showcasing cross-dataset queries enabled by shared entity identifiers. . These sites currently consume our prototype API, providing immediate validation of the integration approach. Develop a minimal demonstration interface displaying Storywrangler Toolbox capabilities and the power of entity-linked datasets.

#### Continuous integration and devlopment practices

Throughout Phase 1, we implement continuous integration and testing infrastructure to ensure code quality and maintainability. Each repository in our GitHub organization includes automated CI/CD pipelines (GitHub Actions) that:

- Run unit and integration tests on every commit
- Validate Pydantic schemas against test datasets
- Build and test container images automatically
- Check code style and documentation completeness
- Generate coverage reports

For the backend API, we implement automated testing that validates:

- Entity ID format validation (Wikidata Q-codes, ORCID, ROR)
- Pydantic schema enforcement
- Database integrity constraints
- API endpoint responses against OpenAPI specification

Each pipeline includes a test suite with sample data, ensuring reproducibility can be verified automatically. This CI/CD infrastructure—established in Phase 1—provides the quality assurance framework for reviewing community submissions in Phase 3. All tests must pass before code is merged, and containers are rebuilt automatically on release.

By refactoring our own pipelines first—including the challenging work of entity matching—we validate that PDP standards are practical and that entity resolution work deserves recognition as scholarly contribution before opening to community submissions in Phase 3.

### Phase 2: Internal interoperability

Phase 2 deepens our infrastructure through partnerships with known collaborators, focusing on lowering barriers to pipeline submission, refining API access patterns, and gathering early feedback. Rather than scaling to broad community adoption, Year 2 concentrates on making integration practical for research groups we already work with, while developing the DevOps practices necessary for sustainable operations.

#### (1) Lowering Barriers: Documentation and Examples

The primary challenge is making integration practical for researchers who already have working projects for their own research needs. Rather than prescribing project structure or requiring researchers to build "Storywrangler pipelines," we demonstrate through real examples how existing research code can be made Storywrangler-compatible with minimal modifications. 

**Example-Driven Documentation:** We develop detailed case studies from our Phase 1 and partner integrations:

- "Integrating the Women in Mathematics biography dataset" (text corpus → entity extraction)
- "Making Wikimedia page view analysis compatible" (existing Node.js/MongoDB project → containerized with adapter)
- "Submitting course catalog analysis" (institutional data → standardized entities)

Each case study shows: (1) the original research project structure (unchanged), (2) the minimal additions needed (adapter code, entity mapping, Dockerfile), and (3) the integration process and design decisions. This approach validates that integration burden is small—researchers maintain full control over their project architecture while gaining Storywrangler compatibility.

**PDP Helper Package Evolution:** We continue developing `pdp-helper` (already pip-installable) as a validation and utility toolkit rather than a scaffolding tool. The package provides:

- Validation commands researchers run on their existing projects (`pdp-helper validate`)
- Entity lookup utilities (Wikidata queries, identifier resolution)
- Schema compliance checking (does output match our time-series format?)
- Container testing (does it build? execute successfully?)

Critically, `pdp-helper` adapts to researchers' project structures rather than dictating them—we provide tooling that works with their conventions (Python/R/Julia, notebooks/scripts, their database choices).

**Standards Repository Validation:** Partner feedback tests whether the Storywrangler Standards Repository clearly communicates the minimal contract: outputs must be time-series data with standardized entity IDs (Wikidata, ORCID, ROR). Everything else—project structure, language choice, internal workflows—remains under researcher control. We iterate on standards documentation based on what partners find confusing or ambiguous.

**Philosophy: Research-First, Integration-Second:** Our target audience builds projects for their own research goals (publications, dissertations, funded grants)—Storywrangler integration is a value-add that enables sharing, citation, and reuse. By demonstrating integration requires minimal modifications to existing projects, we lower adoption barriers and ensure researchers maintain ownership of their work.

#### (2) API Refinement and Multi-Tiered Access

Phase 2 focuses on operationalizing the three-tier access model and ensuring our API can handle diverse usage patterns without degradation. The core challenges are authentication, determining appropriate aggregation levels, and preventing abuse.

**Authentication and Access Control:** We implement token-based authentication and test the boundaries between access tiers with partner datasets. Partners help us determine: What level of aggregation is safe for public access? What requires a data use agreement? What needs approval? These decisions emerge from real sensitivity constraints (copyright, privacy, commercial agreements) rather than abstract policies.

**Rate Limiting and Resource Management:** We implement throttling mechanisms that prevent individual users from degrading service for others, monitor resource consumption patterns, and establish fair-use policies. Partner usage in Phase 2 helps us calibrate reasonable limits and identify expensive query patterns that need optimization or restriction.

**Endpoint Design and Optimization:** Partner research questions drive which endpoints we build and how we structure responses. We monitor which queries are slow, which consume excessive resources, and where database optimization (indexing, caching, pre-computation) is needed. This data-driven approach ensures we invest optimization effort where it matters rather than prematurely optimizing hypothetical use cases.

#### (3) Minimal User Interface for Exploration

Develop a basic web interface enabling non-technical users to discover what data is available and understand what Storywrangler offers. The interface provides dataset browsing (what corpora exist, what time ranges, what entities are covered), basic visualization through Storywrangler Toolbox integration (Allotaxonometer, temporal plots), and simple data export. The goal is demonstrating capabilities and gathering feedback on what researchers actually need, not building a full-featured analysis platform. Partners help us understand: Is this useful? What's missing? What would make them use the web interface versus API?

Throughout Phase 2, we maintain regular contact with partner groups through multiple channels: monthly virtual office hours where partners demo their work and report issues, a Slack channel for quick questions, and GitHub issues for tracked bug reports and feature requests. Quarterly check-ins with each partner provide structured reflection on what's working and what barriers remain. This continuous feedback loop—capturing both informal observations and formal evaluations—directly shapes our infrastructure refinements and informs Phase 3's broader rollout. By engaging partners as collaborators rather than passive users, we ensure Storywrangler develops in response to real research needs. By the end of Year 2, we will have validated our infrastructure with ≥3 partner pipelines, refined our API based on real usage patterns, and gathered structured feedback that directly informs Phase 3's open community rollout.

## 2025-11-15: Plan section 3

#### Overview

Computational social science faces a reproducibility crisis: datasets suffer link rot, pipelines break when APIs change, and archived datasets become isolated artifacts. Current practice treats data as one-off outputs rather than living, maintainable infrastructure. This project addresses these challenges by transforming Storywrangler from a dispersed set of tools and datasets into an ecosystem of **principled data pipelines (PDP)**. 

Borrowing the term from the Human Rights Data Analysis Group, PDP is a philosophy for implementing data workflows as modular scripts, each taking a single input, producing a single output, and having a single, well-defined responsibility. This approach ensures pipelines are **transparent** (each task is reviewable), **auditable** (each step can be tested), and **reproducible** (same inputs yield same outputs across different computing environments). The PDP philosophy aligns with FAIR principles while providing concrete implementation practices familiar to data engineers as Extract, Transform, Load (ETL) patterns, adapted for scientific reproducibility.

Rather than treating pipeline outputs as isolated files for one-off use, we integrate approved pipelines into the Storywrangler ecosystem as ongoing data sources. Upon approval—contingent on pipelines being **runnable as a single step** with clear documentation—pipelines are cloned to our cyberinfrastructure, containerized using Podman, and integrated via custom adapter code (Figure 1). The adapter transforms pipeline outputs to conform to our API schema—standardized time-series formats with Pydantic validation—without modifying the researcher's original code. This separation preserves researchers' workflows while ensuring all pipeline outputs interoperate seamlessly across the Storywrangler platform. Additionally, researchers can opt to have their pipelines receive DOIs via UVM Dataverse, enabling citation as scholarly products.

Our infrastructure supports tiered data access controls that balance openness with privacy and licensing requirements. Pipeline outputs inherit base license terms from source repositories, but submitters can specify additional access restrictions based on data sensitivity. We implement three access tiers: (1) **Public endpoints** providing aggregated, non-identifying statistics accessible to all users; (2) **Authenticated access** for registered researchers requiring more granular data under data use agreements; and (3) **Restricted access** for approved collaborators only. Critically, raw proprietary data (e.g., copyrighted texts, confidential records) remains secured within containerized execution environments and is never exposed via API—only derived, transformative outputs are shared. This enables analysis of sensitive or proprietary sources while respecting copyright and privacy constraints. Phase 1 validates this model with proprietary datasets (Wikimedia, Legacy.com obituaries), demonstrating that commercial data use agreements and open science principles can coexist through appropriate access tiering.

Unlike traditional data repositories that archive static datasets, or code repositories that share unmaintained scripts, Storywrangler maintains living pipelines—continuously executable, version-controlled workflows that serve as both scholarly products and ongoing data sources. This infrastructure transforms Storywrangler from a collection of isolated tools into an interconnected ecosystem where datasets can reference and build upon each other. Rather than researchers repeatedly solving the same data integration problems, Storywrangler provides a growing library of validated, interoperable pipelines that accelerate computational social science research.

We implement this vision through four coordinated phases: Consolidation, Interoperability, Engagement, and Sustainability. Each phase addresses a critical dimension of platform development, beginning with organizing and documenting existing resources, to seamless integration of tools and workflows, to expanding user engagement and community participation, and then the creation of a ecosystem of modular, open-source instruments. Focusing on principled data pipelines will provide strong guarantees of **data auditability**, **interoperability**, and **better privacy controls**—turning Storywrangler from a collection of isolated datasets into an integrated data ecosystem.


## 2025-11-12: fleeting notes

Here's a few prompts i need to think about:

#### Discussing CompStoryLab projects (§2; ft. Michael)

Similar to how the health team have been doing it; storywrangler (tweets), allotax, ousiometer, 

#### _Submitting (principled) data pipelines not datasets_ (§3? ft. SamZ)

- [[Submitting data pipelines]]

Users should be able to submit (principled) data pipelines not just datasets. Why? What would they look like? What's the problem with just having datasets?

First off, we can totally accept datasets. For instance, people provide a new book and we analyze them with our tools through our tools (storywrangler). This is fine. But this is limited in the following sense; the datasets will each live on their own little island, not talking to each other. If our goal is to build a more integrated data platform, we need some curation process by which datasets are standardized. 

First off, one thing is that it might be easier to just sell it as users "can submit a documented, reproducible data pipeline as part of their dataset submission". That is, users could submit a repo (like Sam's [faculty trajectories one](https://github.com/samzhang111/faculty-trajectories)) implementing PDP (in some form), that we could review and "test" to some degree. Hence, we could have some degree of **data auditability**.

 Obviously, testing and reviewing pipelines will be a limiting factor, but arguably it is better to have fewer, high quality datasets than more junk. Additionally, if we’re happy given some criteria, we could integrate the final output as part of API endpoint, that we would be in charge of hosting. That way, we can improve on the **interoperability** aspect, where we would make our different endpoints talk to each other given a formal standards. This approach reduces the number of datasets, but allow us to potentially build a more integrated data ecosystems.

Another benefit of accepting principled pipelines that integrate with our API is that we can provide some guarantee in terms of data privacy. Say that some groups want to share their data, but don't want to make  it public. One benefit of working with data pipelines is that the raw data don't need to be materialized anywhere; it is locked in on our database and accessible only via the API. The endpoints can then provide more focused, and private data representations of the data. We can manage the token auth process, whereas we provide permission to trusted individuals to access more or less raw datasets.

#### _Deliverables_ (§4.1)

What communication strategies we can use to draw attention from the general public and other researchers to our tools?

- *Not the Pudding:* 
	- We have a scientific core to our data visualization while the Pudding is more journalistic by nature. 
	- Hence, our set of interactive data visualizations builds on top of original work, instead of being reported. For instance, the allotaxonograph is a set of tools unique to our lab, implementing stories based on it go beyond reporting a story. 
	- Additionally, we use our scientific work to drive the story that we tell, as with interactive press releases. We mesh together our scientific works with interactive data essays to communicate original results.  
- *Why scrollytelling as narrative device?*

#### Teaching complex systems via our principled tools in classrooms (§?)

## 2025-11-11: fleeting notes

- Providing the right *data model* is a key challenge for a couple of reasons. 
	- We simply define data model as (useful) representation of the data that stands in relationships with some real-world phenomena. 
	- Arguably there is no objective data model; raw data itself is useless. There needs to be work put into any kind of data to be able to extract insights.  Data itself must be understood as such; as the saying goes, no "data makes sense except in the light of evolution" (or something like that).
	- Now, lets focus on the following challenges
		1. `data size and throughput`: Drinking from a fireman hose can be dangerous; similarly, taming big data requires care and resources. 
			- It is understood that the nature of big data coevolve with that of our hardware and software; as chips are becoming smaller and more performant, and laptop increase random access memory, what used to be big is not tiny. As of today, we can decompose big data at least in terms of **storage** and **compute**. 
			- But for all practical purpose, big data is getting big when we are talking about terabytes of data. According to a [recent duckdb user survey](https://duckdb.org/docs/stable/guides/performance/working_with_huge_databases), used by a huge swaths of data engineers, people rarely need to handle big datasets. 56% of people work typically with <16GB while 61% work with 512GB< (see [here](https://duckdb.org/2024/10/04/duckdb-user-survey-analysis#dataset-sizes))., leading duckdb folks to say that [big data is dead](https://motherduck.com/blog/big-data-is-dead/). 
			- Although people often focus on the information aspect of big data, here we also the social and institutional aspect of big data; to get access and analyze big data, one needs resources and expertise that are beyond any given individual.
		2. `data quality`: as already state, having more of the same data is not helpful. But one can have quality dataset without retuning into tiny dataset world (see [FineWeb: high-quality web-scale dataset for LLM pretraining](https://huggingface.co/spaces/HuggingFaceFW/blogpost-fineweb-v1)). Some big data can be better than others at particular tasks, such as training classifiers.   A few quality comes out of this line of inquiry:
			1. *Base filtering in text analysis*: removing boiler plate, or lower quality data. This is finicky and often depends on the research question.
			2. *Deduplicated datasets* are key to training machine learning models.
		3. `thick data`: this is qualitative data about people; recording their experience, conversation outcomes, feelings, reactions. This typically comes only in small-scale version, as collecting thick data is often unstructured and requires manual labor. One of the largest, arguably more thick data might be something like the [candor corpus](https://www.science.org/doi/10.1126/sciadv.adf3197), containing 1656 conversations recorded in spoken English (1 TB of audio, video, and transcripts, with moment-to-moment measures of vocal, facial, and semantic expression, together with an extensive survey of speakers’ postconversation reflections).
		4. `data mutation`: people sometimes want to make changes to their dataset; add a feature, clean up a variable name, join. Data mutation might be inversely proportional to data size in that larger datasets already are characterized by impersonal population summarized with a large number of features; think of Twitter. Data mutation can happen, but most likely on some relevant subsets of the full dataset. When doing survey work or supervise machine learning, data engineering is the bread and butter of scientists. 
		5. `data interoperability` (see also [[Working with APIs]]): in and of itself, any given dataset can be interesting. But how do any data can be merged with additional data is the oil of the information economy. This can be thought as subpoint  to `data mutation`, but here the focus is in providing standard format so that different stakeholders can talk to each other. 
			1. It can be at the API level itself; for instance, [openAPI](https://www.openapis.org/) is a spec that provide a standard description of HTTP APIs; GET, POST, UDPATE, DELETE. 
			2. Or domain-specific, such as with the [openAG alliance](https://openag.io/)(see [this slide deck](https://openag.io/oada-docs/intro/OADA_API_Intro_Trellis.html#1) for an intro). A key point with API is that it can help with decentralizing data sharing in a way that is secure and trustworthy for different stakeholders; everybody just need to agree on a common format, which typically requires institutional process with proper governing bodies.
		6. `data openness`: most big datasets--governmental, google, facebook, etc--are also closed. Some used to be more open (twitter) but have since been closed down. Some big-gish datasets exist, e.g. wikipedia, semantic scholar (220M paper metadata, full citation graph, > 15M fully parsed articles, metadata of all sorts), which are freely available but can be finicky to work with.
		7. `ethical data`: underlying text data are people, who might or might not have given the consent for their data to be used. When collecting from afar, we might have a sense of objectivity; but this might be misleading. More of the same data does not equate objectivity, especially when it comes to social media platform where data acquisition is always mediated by some kind of medium that might distort reality. 
		8. `data pipeline maintainability`:


### Misc refs
- https://huggingface.co/datasets/allenai/c4 mentioned in [[FineWeb]] article as old but gold. AllenAI host a 2.3 TB version of the c4 dataset on huggingface.