# Horizon Daily - 2026-06-16

> From 17 items, 13 important content pieces were selected

---

1. [John Carmack Praises Fabrice Bellard's Genius](#item-1) ⭐️ 9.0/10
2. [x86 Emulator Team Fixed Bad Code During Emulation](#item-2) ⭐️ 8.0/10
3. [Backdoor in LinkedIn Job Offer via npm Prepare Script](#item-3) ⭐️ 8.0/10
4. [Iroh 1.0: P2P Networking Library for Apps](#item-4) ⭐️ 8.0/10
5. [Hacker News Users Share Local LLM Coding Setups](#item-5) ⭐️ 8.0/10
6. [Simple 'fix this code' prompt jailbreaks Fable 5 AI](#item-6) ⭐️ 8.0/10
7. [Hetzner Announces Major Cloud Server Price Hike](#item-7) ⭐️ 7.0/10
8. [Exploring the Technical Feasibility of a Peopleless Economy](#item-8) ⭐️ 7.0/10
9. [Banned Book Library Hidden in a Wi-Fi Smart Light Bulb](#item-9) ⭐️ 6.0/10
10. [TinyWind: Pixel Pirate Sailing Game with Wind Physics](#item-10) ⭐️ 6.0/10
11. [Nostalgic Reflection on Love for Computers](#item-11) ⭐️ 6.0/10
12. [Commodore Announces Flip Phone with Sailfish OS](#item-12) ⭐️ 6.0/10
13. [Datasette Agent 0.3a0 Adds Write SQL with User Approval](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [John Carmack Praises Fabrice Bellard's Genius](https://twitter.com/ID_AA_Carmack/status/2064095424420487226) ⭐️ 9.0/10

John Carmack tweeted about Fabrice Bellard, sparking a high-engagement discussion on Hacker News about Bellard's remarkable contributions and work ethic. This highlights the deep respect within the tech community for Bellard's prolific output, including FFmpeg, QEMU, and QuickJS, and underscores the value of focused, independent development. The discussion noted Bellard's ability to turn complex specifications into high-performance C code, and mentioned his recent project ts_zip, which uses LLMs for text compression.

hackernews · apitman · Jun 16, 04:58 · [Discussion](https://news.ycombinator.com/item?id=48550779)

**Background**: Fabrice Bellard is a French computer programmer known for creating foundational open-source projects like FFmpeg, QEMU, and TinyCC. He is widely regarded as one of the most talented programmers in the world, often working alone on ambitious projects.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Fabrice_Bellard">Fabrice Bellard - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=46377862">Fabrice Bellard: Biography (2009) [pdf] | Hacker News</a></li>

</ul>
</details>

**Discussion**: Commenters expressed admiration for Bellard's work ethic and privacy, with some comparing his anonymity to Satoshi Nakamoto. Others noted that much of his work involves translating specifications into efficient C code, which is still highly impressive.

**Tags**: `#Fabrice Bellard`, `#John Carmack`, `#programming`, `#open source`, `#Hacker News`

---

<a id="item-2"></a>
## [x86 Emulator Team Fixed Bad Code During Emulation](https://devblogs.microsoft.com/oldnewthing/20260615-00/?p=112419) ⭐️ 8.0/10

The x86 emulator team at Microsoft encountered a program that allocated 64KB of stack memory using an inefficient loop unrolling technique, and they patched the emulator to optimize this initialization during emulation, improving performance. This story highlights how compatibility layers and emulators can work around poorly written software to improve user experience, a practice still relevant today with tools like Proton and Wine for Linux gaming. The program used a loop unrolling pattern that initialized memory in 256KB chunks instead of a tight loop, which was slower. The emulator team modified the emulation to recognize this pattern and replace it with a more efficient initialization.

hackernews · paulmooreparks · Jun 16, 04:46 · [Discussion](https://news.ycombinator.com/item?id=48550693)

**Background**: Emulators and compatibility layers often need to mimic the behavior of original hardware or operating systems. Sometimes, poorly written software can run inefficiently on these layers, prompting developers to add workarounds that improve performance without changing the original code.

<details><summary>References</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/oldnewthing/20100311-00/?p=14643">Application compatibility layers are there for the customer,</a></li>

</ul>
</details>

**Discussion**: Commenters shared similar stories, such as Microsoft patching SimCity's read-after-free bug in Windows 95, and noted that modern compatibility layers like Proton and Wine now incorporate hotfixes for poorly ported games like Elden Ring. Some questioned the technical reasoning behind the loop unrolling, suggesting it might have been faster on certain hardware.

**Tags**: `#emulation`, `#x86`, `#compatibility`, `#software engineering`, `#historical anecdote`

---

<a id="item-3"></a>
## [Backdoor in LinkedIn Job Offer via npm Prepare Script](https://roman.pt/posts/linkedin-backdoor/) ⭐️ 8.0/10

A security researcher discovered a backdoor hidden in a GitHub repository sent by a recruiter during a LinkedIn job interview process, which exploits npm's prepare script to execute arbitrary code upon dependency installation. This incident highlights a novel social engineering attack vector targeting software engineers through fake job offers, potentially leading to supply chain compromises and data theft. It underscores the need for better reporting mechanisms and awareness of npm script execution risks. The backdoor was embedded in a public GitHub repository under the guise of a broken proof-of-concept, with the malicious code hidden within commented-out tests. npm's prepare script runs automatically after npm install, so simply installing dependencies triggers the backdoor.

hackernews · lwhsiao · Jun 15, 20:00 · [Discussion](https://news.ycombinator.com/item?id=48546294)

**Background**: npm is a package manager for Node.js that allows developers to define scripts in package.json, including 'prepare', which runs automatically after 'npm install'. Supply chain attacks on npm have become increasingly common, where malicious packages or scripts are used to compromise developer machines or downstream users. Social engineering via LinkedIn is a growing trend, where attackers pose as recruiters to trick developers into executing malicious code.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.phor.net/npm-zero-day-npm-installation-runs">NPM zero-day: npm installation runs unspecified scripts with</a></li>
<li><a href="https://blog.sandworm.dev/dissecting-npm-malware-five-packages-and-their-evil-install-scripts">Dissecting Npm Malware: Five Packages And Their Evil Install</a></li>
<li><a href="https://cybersecuritynews.com/github-automated-disable-npm-script-installs/">GitHub to Automated Disable npm Script Installs to Block Supply</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern about the lack of a centralized reporting system for cybercrime, with one noting that LinkedIn and GitHub often fail to act on such reports. Some speculated that the writeup might be AI-generated, while others shared personal experiences of nearly falling for similar sophisticated attacks.

**Tags**: `#security`, `#supply chain attack`, `#social engineering`, `#npm`, `#LinkedIn`

---

<a id="item-4"></a>
## [Iroh 1.0: P2P Networking Library for Apps](https://www.iroh.computer/blog/v1) ⭐️ 8.0/10

Iroh 1.0 has been released as a peer-to-peer networking library that enables direct connections between app instances without requiring a VPN, featuring extensible transport support. This simplifies application-layer connectivity for developers, similar to how Tailscale simplifies network-layer connectivity, potentially enabling easier development of decentralized and collaborative apps. Iroh 1.0 supports IPv4, IPv6, and relay transports out of the box, and allows custom transport implementations. It uses cryptographic keys for identity and encrypted traffic via relay servers.

hackernews · chadfowler · Jun 15, 15:13 · [Discussion](https://news.ycombinator.com/item?id=48542480)

**Background**: Peer-to-peer networking allows devices to communicate directly without a central server. Iroh is a Rust-based library that provides a high-level API for establishing such connections, handling NAT traversal and relay fallback automatically.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.rs/iroh/latest/iroh/">iroh - Rust</a></li>
<li><a href="https://kalilinuxtutorials.com/iroh/">Iroh : The Future Of Decentralized Networking Technology</a></li>

</ul>
</details>

**Discussion**: The community compared Iroh to Tailscale at the application layer, with developers clarifying that Iroh uses cryptographic keys for identity and supports custom transports. Some users questioned where peer-to-peer connections actually work, while others appreciated the extensibility.

**Tags**: `#peer-to-peer`, `#networking`, `#rust`, `#open-source`, `#library`

---

<a id="item-5"></a>
## [Hacker News Users Share Local LLM Coding Setups](https://news.ycombinator.com/item?id=48542100) ⭐️ 8.0/10

Hacker News users are sharing their experiences replacing cloud-based coding assistants like Claude and GPT with local models, detailing specific setups, performance metrics, and trade-offs. This discussion highlights a growing trend among developers seeking privacy, cost savings, and independence from cloud services, while also revealing the current limitations of local models compared to frontier models. Users report using models like Qwen3.6 35B and Gemma 4 26B on hardware such as Mac Studio with 128GB RAM or dual RTX 3090s, achieving speeds around 150 tok/s. Some still fall back to cloud models for complex tasks.

hackernews · cloudking · Jun 15, 14:46

**Background**: Local LLMs run entirely on a user's own hardware, offering privacy and offline capability but often with lower performance than cloud-based models. Tok/s (tokens per second) measures generation speed, with higher values indicating faster responses.

<details><summary>References</summary>
<ul>
<li><a href="https://www.xda-developers.com/finally-found-local-llm-want-use-coding/">I finally found a local LLM I actually want to use for coding</a></li>
<li><a href="https://codesamplez.com/productivity/local-ai-coding-agent">Local LLM for Coding: Free AI Coding Agent With Ollama + Claude</a></li>
<li><a href="https://benchlm.ai/llm-speed">LLM Speed & Latency Comparison — Tokens/sec &</a></li>

</ul>
</details>

**Discussion**: The community is divided: some users successfully replaced cloud assistants for most tasks, citing privacy and cost benefits, while others argue the performance gap is still too large to justify the switch. A user named codinhood notes the opportunity cost of not using the latest models is too high.

**Tags**: `#local LLM`, `#coding assistant`, `#privacy`, `#open source`, `#AI tools`

---

<a id="item-6"></a>
## [Simple 'fix this code' prompt jailbreaks Fable 5 AI](https://www.theregister.com/security/2026/06/15/feds-freaked-over-fable-5-after-simple-fix-this-code-prompt-not-jailbreak-says-researcher/5255827) ⭐️ 8.0/10

A researcher found that asking Anthropic's Fable 5 AI model to 'fix this code' can generate exploit code without using a traditional jailbreak prompt. This technique bypasses safety guardrails by framing the request as a benign code-fixing task. This discovery highlights a fundamental vulnerability in LLM safety measures, as the 'fix this code' approach is both trivial to execute and nearly impossible to patch without crippling the model's utility. It also raises serious concerns about export controls, since such a simple bypass could allow adversaries to generate cyber weapons. The technique does not require a jailbreak; instead, it exploits the model's training to assist with code improvement. The researcher noted that the model produces exploit code as part of 'test cases' to verify the fix, making the vulnerability hard to eliminate.

hackernews · _tk_ · Jun 16, 09:26 · [Discussion](https://news.ycombinator.com/item?id=48552687)

**Background**: LLM jailbreaks are methods to trick AI systems into bypassing their built-in safety rules. Traditional jailbreaks use clever prompts to override restrictions, but the 'fix this code' approach is novel because it frames the malicious request as a legitimate programming task. Export controls on AI models aim to prevent adversaries from accessing powerful AI capabilities, but this finding shows that even models with safety guardrails can be easily misused.

<details><summary>References</summary>
<ul>
<li><a href="https://adversa.ai/blog/universal-llm-jailbreak-chatgpt-gpt-4-bard-bing-anthropic-and-beyond/">Universal LLM Jailbreak: ChatGPT, GPT-4, BARD, BING, Anthropic,</a></li>

</ul>
</details>

**Discussion**: Commenters expressed mixed reactions: some praised the elegance of the 'fix this code' jailbreak as both trivial and unfixable, while others argued that the government's concern is politically motivated retaliation against Anthropic. There was also debate about Anthropic's contradictory stance of claiming Fable is extremely dangerous while releasing it with imperfect safety measures.

**Tags**: `#AI safety`, `#jailbreak`, `#LLM`, `#Anthropic`, `#cybersecurity`

---

<a id="item-7"></a>
## [Hetzner Announces Major Cloud Server Price Hike](https://docs.hetzner.com/general/infrastructure-and-availability/price-adjustment/#cloud-servers) ⭐️ 7.0/10

Hetzner, a major European cloud provider, announced a significant price increase for its cloud servers, with some reports indicating up to a 3x jump. The new pricing took effect shortly after a previous adjustment 38 days ago. This price hike affects many small and medium businesses that rely on Hetzner for affordable cloud infrastructure, and it signals broader hardware cost inflation across the industry. The community's strong reaction (486 points, 674 comments) underscores the impact on the developer ecosystem. The price increase applies to Hetzner's cloud server product line, with some configurations seeing a 3x rise. Hetzner's CEO cited unchanged pricing strategy for years and rising hardware and operational costs as reasons.

hackernews · tuhtah · Jun 15, 13:19 · [Discussion](https://news.ycombinator.com/item?id=48540844)

**Background**: Hetzner is a German hosting company known for offering competitive prices on dedicated servers and cloud instances. The cloud market has seen rising costs due to global chip shortages, increased demand for RAM and storage, and inflation. Hyperscalers like AWS, GCP, and Azure have more leverage in supply chains, but smaller providers like Hetzner are more exposed to market fluctuations.

**Discussion**: The community is divided: some users express shock at the 3x increase, questioning the justification, while others note that Hetzner's prices were unsustainably low and that hardware costs have indeed risen sharply. A few commenters point out that this may reduce the cost advantage Hetzner had over larger competitors.

**Tags**: `#cloud`, `#pricing`, `#Hetzner`, `#infrastructure`, `#economics`

---

<a id="item-8"></a>
## [Exploring the Technical Feasibility of a Peopleless Economy](https://gmalandrakis.com/writings/ad-economicum.html) ⭐️ 7.0/10

An article titled 'Peopleless economy? Not technically impossible' examines whether a fully automated economy could function without human labor, arguing that it is technically feasible but challenges societal assumptions about work and consumption. This discussion is significant because it questions the foundational belief that human labor is essential for economic activity, which has profound implications for employment, social welfare, and the future of capitalism. The article critiques common assumptions about automation, such as the necessity of consumer demand to motivate work, and suggests that governments may resort to oppressive measures if mass unemployment occurs.

hackernews · l0new0lf-G · Jun 15, 21:10 · [Discussion](https://news.ycombinator.com/item?id=48547062)

**Background**: The concept of a 'peopleless economy' refers to a system where production and distribution are fully automated, eliminating the need for human workers. This idea is often discussed in the context of AI and robotics advancements, raising questions about income distribution and social stability.

**Discussion**: Comments highlight frustration with predicting the future, skepticism about consumer-based economies, and a debate on whether engineers or economists are better suited to analyze AI's economic impact. Some argue that governments would not simply abandon democracy in the face of automation.

**Tags**: `#AI`, `#economics`, `#automation`, `#future of work`

---

<a id="item-9"></a>
## [Banned Book Library Hidden in a Wi-Fi Smart Light Bulb](https://www.richardosgood.com/posts/banned-book-library/) ⭐️ 6.0/10

A developer repurposed a Wi-Fi smart light bulb to host a library of commonly banned books, accessible via the bulb's own Wi-Fi network without an internet connection. This project demonstrates a creative use of IoT devices for offline information sharing, potentially enabling access to restricted content in areas with censorship. The light bulb runs a lightweight web server and hosts a curated list of books often labeled as banned; it is inspired by the PirateBox concept but embedded in a smart bulb form factor.

hackernews · sohkamyung · Jun 15, 22:37 · [Discussion](https://news.ycombinator.com/item?id=48547985)

**Background**: A PirateBox is a portable device that creates a local Wi-Fi network for anonymous file sharing, often used to distribute information without internet access. This project adapts that idea to a smart light bulb, which typically runs Linux and can be customized.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PirateBox">PirateBox - Wikipedia</a></li>
<li><a href="https://daviddarts.com/piratebox/">David Darts - PirateBox</a></li>
<li><a href="https://torrentfreak.com/piratebox-takes-file-sharing-off-the-radar-and-offline-for-next-to-nothing-120311/">PirateBox Takes File-Sharing Off The Radar and Offline, For</a></li>

</ul>
</details>

**Discussion**: Commenters noted the similarity to PirateBox and questioned whether the listed books are truly banned, with some arguing they are merely removed from school libraries for explicit content. Others expressed interest in the book list but doubted it includes truly controversial works.

**Tags**: `#Wi-Fi`, `#smart light bulb`, `#banned books`, `#PirateBox`, `#DIY`

---

<a id="item-10"></a>
## [TinyWind: Pixel Pirate Sailing Game with Wind Physics](https://tinywind.io/) ⭐️ 6.0/10

TinyWind is a pixel art sailing game that simulates wind physics, allowing players to sail across procedurally generated oceans. The game has recorded over 380,000 kilometers sailed by its community. This game explores the potential of wind physics in gaming, offering a unique sailing experience that could inspire more realistic nautical games. However, community feedback indicates the physics are not fully realistic, highlighting the challenge of balancing fun and accuracy. The game features a wind teller indicator, sail angle adjustment, and combat with enemy ships. Players have noted that the wind direction indicator is unintuitive and that sail trim mechanics feel clunky and unresponsive.

hackernews · tinywind · Jun 15, 16:15 · [Discussion](https://news.ycombinator.com/item?id=48543475)

**Background**: Sailing games often simplify wind physics for accessibility, but realistic wind simulation involves complex factors like apparent wind, tacking angles, and sail trim. TinyWind attempts to incorporate these elements in a pixel art format, appealing to both gamers and sailing enthusiasts.

**Discussion**: Community comments are mixed: some praise the game's concept and fun factor, while others criticize the wind physics as unrealistic and the controls as clunky. Specific feedback includes requests for clearer wind indicators, better sail trim mapping, and more realistic upwind performance.

**Tags**: `#game`, `#sailing`, `#wind physics`, `#web game`

---

<a id="item-11"></a>
## [Nostalgic Reflection on Love for Computers](https://michaelenger.com/blog/i-love-the-computer/) ⭐️ 6.0/10

Michael Enger published a personal blog post titled 'I Love the Computer,' reflecting on his lifelong passion for computers and how the computing landscape has changed over time. The article resonates deeply with the tech community, sparking a discussion about nostalgia, the evolution of computing, and the tension between loving the machine and disliking the modern industry. The post scored 6.0/10 in technical depth but achieved high engagement with 255 points and 147 comments, indicating strong community resonance despite lacking novelty.

hackernews · speckx · Jun 15, 20:14 · [Discussion](https://news.ycombinator.com/item?id=48546441)

**Background**: The article is a personal reflection, not a technical piece. It taps into a common sentiment among older programmers and enthusiasts who feel that modern computing has lost some of its magic.

**Discussion**: Comments express a mix of nostalgia and critique: some agree that the spark is gone, while others argue that AI and modern tools still offer wonder. A few commenters distinguish between loving the computer and disliking the industry.

**Tags**: `#nostalgia`, `#computing`, `#personal reflection`, `#community discussion`

---

<a id="item-12"></a>
## [Commodore Announces Flip Phone with Sailfish OS](https://commodore.net/why-a-flip-phone/) ⭐️ 6.0/10

Commodore has announced a flip phone running Sailfish OS with Android app compatibility, targeting users seeking a simpler smartphone experience. This device offers a middle ground between feature phones and full smartphones, appealing to privacy-conscious users and those wanting to reduce screen time without losing essential apps like WhatsApp and maps. The phone is priced at $500, which has drawn criticism from the community. It features a retro camera design and runs Sailfish OS, a Linux-based European alternative to mainstream mobile operating systems.

hackernews · bartekrutkowski · Jun 16, 09:15 · [Discussion](https://news.ycombinator.com/item?id=48552614)

**Background**: Sailfish OS is developed by Jolla and is known for its privacy-focused approach and gesture-based interface. It supports Android app compatibility through a compatibility layer, allowing access to a wide range of apps. Commodore, a historic brand in computing, is leveraging its brand recognition to enter the mobile market.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sailfish_OS">Sailfish OS - Wikipedia</a></li>
<li><a href="https://sailfishos.org/">Sailfish OS - European alternative for Mobile operating systems</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed: some express interest in Sailfish OS and the 'dumb phone' concept, while others are skeptical, suggesting it may be a rebranded ODM device and criticizing the $500 price point. There is also concern about the lack of detail and the retro camera design.

**Tags**: `#mobile`, `#Sailfish OS`, `#privacy`, `#flip phone`, `#Commodore`

---

<a id="item-13"></a>
## [Datasette Agent 0.3a0 Adds Write SQL with User Approval](https://simonwillison.net/2026/Jun/15/datasette-agent/#atom-everything) ⭐️ 6.0/10

Datasette Agent 0.3a0 introduces the execute_write_sql tool, which requests user approval before executing write operations on a database. The release also enhances the CLI chat mode to support approvals and adds --unsafe mode for auto-approval. This update makes Datasette Agent safer for real-world use by adding a permission layer for write operations, enabling users to confidently let the AI modify databases. It bridges the gap between AI convenience and data integrity, which is crucial for adoption in production environments. The execute_write_sql tool respects user permissions and shows a confirmation dialog with the exact SQL statements and parameters before execution. The --unsafe mode bypasses all approvals, while --yes approves all questions without the root privilege escalation.

rss · Simon Willison · Jun 15, 17:19

**Background**: Datasette Agent is an open-source plugin for Datasette that integrates large language models (LLMs) to provide an AI assistant for interacting with SQLite databases. It supports hundreds of tool-calling models from vendors like OpenAI. The execute_write_sql tool builds on the approval mechanism introduced in version 0.2a0.

<details><summary>References</summary>
<ul>
<li><a href="https://datasette.io/blog/2026/datasette-agent/">Datasette Agent, an extensible AI assistant for Datasette -</a></li>
<li><a href="https://datasette.io/">Datasette: An open source multi-tool for exploring and</a></li>

</ul>
</details>

**Tags**: `#datasette`, `#SQL`, `#open source`, `#tooling`

---

